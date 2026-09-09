# Templates n8n — entretien vault + RAG (public · sanitisé)

> **Démo publique.** Placeholders only. Pas de chemins disque réels, pas de secrets, pas d’IDs d’instance live.

## Idée en une phrase

**n8n orchestre** (planning / webhook).  
Les **scripts Windows** font le travail (collecte, index RAG, backup).  
Un **pont HTTP local** relie les deux, parce que n8n en Docker **ne voit pas** ton disque.

```
n8n (Docker)
   schedule / webhook
        |
        |  GET  /health
        |  POST /run/...   + token
        v
Pont hôte (localhost)
        |
        v
Scripts PowerShell (allowlist)
   collect  |  RAG delta  |  backup git (option)
```

Ce n’est **pas** un « watch dossier → lance tout » pour le vault.  
Les templates de collecte / RAG delta ici sont déclenchés par **horaires**.

## Fichiers

| Fichier | Rôle |
|---|---|
| [`workflow-vault-collect-schedule.json`](workflow-vault-collect-schedule.json) | Cron → probe pont → `POST …/run/local-sync` |
| [`workflow-vault-rag-delta-schedule.json`](workflow-vault-rag-delta-schedule.json) | Heures paires → probe → `POST …/run/rag-cursor-delta` |
| [`workflow-rag-query-filtered.json`](workflow-rag-query-filtered.json) | Webhook query RAG avec filtre de zones (exemple) |
| [`zones.example.json`](zones.example.json) | Motifs d’exclusion **exemples** (à remplacer en privé) |
| [`bridge-allowlist.example.md`](bridge-allowlist.example.md) | Contrat du pont (endpoints allowlist) |

## Variables d’environnement (n8n)

À définir dans ton `.env` n8n (jamais commités) :

| Variable | Exemple | Usage |
|---|---|---|
| `VAULT_BRIDGE_BASE_URL` | `http://host.docker.internal:39790` | Base du pont hôte |
| `VAULT_BRIDGE_TOKEN` | *(secret local)* | Header `X-Vault-Bridge-Token` |

Les workflows publics lisent ces variables. Adapte le port / l’hôte à ton lab.

## Comment importer

1. Dans n8n : **Workflows → Import from File**.
2. Choisir un des JSON.
3. Renseigner les variables d’env.
4. Laisser **`active: false`** jusqu’à ce que le pont réponde `GET /health` → 200.
5. Activer seulement après un test manuel du pont.

## Ce que ça ne publie pas

- Noms de dossiers vault réels  
- Tokens / Bearer  
- Chemins `D:\…`  
- Identifiants d’agents ou de machines  
- Sorties Graphify / graphes perso  

La liste d’exclusion **privée** (zones sensibles) reste hors de ce dépôt. Voir seulement `zones.example.json`.

## Lien avec le reste du template

- Parcours Obsidian + RAG : [`../README.md`](../README.md)  
- Carte structurelle optionnelle : [`../GRAPHIFY.md`](../GRAPHIFY.md)  
- Ops réels (scripts, pont) : repo **privé** côté lab (pas ici)
