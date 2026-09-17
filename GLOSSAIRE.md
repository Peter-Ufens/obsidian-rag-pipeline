# Glossaire (français simple)

> **Ce fichier n’est PAS** le glossaire de recherche privé (vocabulaire dicté),  
> **ni** le « lexique évolutif » (outil d’observation / backtest, STOP après G2).  
> Ici : **lexique pédagogique** pour lire le template et les docs publiques.  
> Mécanisme de lecture du glossaire privé : dépôt public [`iris-mcp-server`](https://github.com/Peter-Ufens/iris-mcp-server) (`rag-search-v2`, variable `RAG_GLOSSARY_FILE`).

| Mot | Signification |
|---|---|
| **Vault** | Le dossier Obsidian qui contient toutes tes notes. |
| **RAG** | Système qui *retrouve* des passages dans tes notes pour répondre plus juste. **Pas besoin de code pour comprendre l’idée** : voir la [série RAG (présentations)](https://github.com/Peter-Ufens/AI-Lab-Journal/tree/main/presentations/RAG-Series). |
| **Ollama** | Programme pour faire tourner des modèles d’IA **sur ton PC**. |
| **Pipeline** | Enchaînement d’étapes automatiques (ex. importer → extraire idées → indexer). |
| **Export** | Fichier (souvent ZIP) qui contient une copie de tes conversations. |
| **Delta** | N’importer que ce qui est **nouveau**, sans tout recopier. |
| **Template** | Modèle vide réutilisable, sans ta vie privée dedans. |
| **Graphify** | Outil qui construit une **carte de liens** entre fichiers / code (structure). **Pas** un RAG. Voir [`GRAPHIFY.md`](GRAPHIFY.md). |
| **graphifyy** | Nom du package PyPI (deux `y`) pour Graphify. |
| **n8n** | Orchestrateur de workflows (souvent en Docker). Ici : déclenche, ne lit pas ton disque directement. |
| **Pont hôte** | Petit serveur HTTP sur le PC qui lance des scripts **allowlist** pour n8n. Voir [`n8n-templates/`](n8n-templates/). |
