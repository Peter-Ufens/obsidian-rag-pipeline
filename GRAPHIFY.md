# Graphify — carte structurelle (optionnel)

> **Public · sans données personnelles.**  
> Graphify **n’est pas** un RAG. C’est une **carte de liens** entre fichiers / symboles d’un projet (ou de plusieurs repos).

## En français simple

| | RAG (ce template) | Graphify |
|---|---|---|
| Question typique | « De quoi parle X ? » | « Qu’est-ce qui pointe vers X ? » / « où vit ce plan ? » |
| Réponse | Passages de texte proches | Liste de **fichiers / nœuds** reliés |
| Données | Contenu des notes | Structure (liens md, imports code, mentions) |

Tu peux avoir **les deux** : RAG pour le sens, Graphify pour la structure.

## Package

Sur PyPI : **`graphifyy`** (deux `y`).

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install graphifyy
```

## Fichiers utiles à ajouter dans *ton* projet

| Fichier | Rôle |
|---|---|
| [`.graphifyignore`](.graphifyignore) | Exclure secrets, PDF, données perso, sorties |
| `CONSIGNES-GRAPHIFY.md` (optionnel) | Statut du dernier run pour un agent / toi |

## Règles de sécurité (importantes)

1. **Ne committe jamais** le dossier de sortie (`graphify-out/`, `graph.json` volumineux).
2. Avant de partager un graphe : cherche les noms, credentials, chemins intimes.
3. Sur un repo **public** : seulement la doc + `.graphifyignore` d’exemple, **pas** ton graphe réel.
4. Graphify ≠ sauvegarde : pour revenir en arrière après une erreur, c’est **git**.

## Exemple de commande (à adapter)

```powershell
# Depuis un venv où graphifyy est installé
graphify extract .\mon-projet --out .\graphify-out\mon-projet
```

Selon la version du CLI, l’extraction markdown peut demander un LLM. Une approche **déterministe** (extracteurs du package sans backend LLM) est possible pour un lab local ; à documenter dans ton repo ops privé.

## Lien avec ce template

Ce dépôt reste centré **Obsidian + RAG**. Graphify est une **brique optionnelle** quand tu veux cartographier plusieurs projets / un monorepo.

Suite côté assistant : [`POUR-ASSISTANT-IA.md`](POUR-ASSISTANT-IA.md).
