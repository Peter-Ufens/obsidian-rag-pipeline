# Pont hôte — contrat d’allowlist (exemple public)

n8n **ne doit pas** exécuter PowerShell arbitraire.  
Le pont n’accepte que des chemins listés.

## Endpoints typiques

| Méthode | Chemin | Effet (côté hôte) |
|---|---|---|
| `GET` | `/health` | Pont vivant · pas de script |
| `POST` | `/run/local-sync` | Collecte conversations → notes vault (léger) |
| `POST` | `/run/rag-cursor-delta` | Index RAG **delta** (souvent « Cursor only » + soft-skip) |
| `POST` | `/run/git-mirror` | Backup / miroir git filtré (option) |

## Sécurité minimale

1. Écouter **localhost** (et éventuellement `host.docker.internal` depuis Docker).  
2. Exiger un **token** header (ex. `X-Vault-Bridge-Token`).  
3. **Allowlist** stricte : un chemin HTTP = un script connu.  
4. Pas de Zone privée / exports bruts sans GO humain.  
5. Timeouts courts sur n8n ; jobs longs côté hôte.

## Soft-skip (RAG delta)

Si aucun fichier source n’a changé (hash tracker), le script peut sortir **0** sans appeler embeddings / vecteurs.  
n8n reçoit quand même un ack HTTP ; le détail est dans le log / rapport hôte.

## Hors scope de ce template public

L’implémentation PowerShell du pont et les scripts restent dans le lab **privé**.
