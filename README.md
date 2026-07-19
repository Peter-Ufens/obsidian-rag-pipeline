# Pipeline Obsidian + recherche intelligente — mode d’emploi simple

> **Public · sans données personnelles.**  
> Pour un profil RH, métier, ou débutant en IA — et pour un assistant (Claude, ChatGPT) qui t’accompagne.

Inspiré du style de [AI-Lab-Journal](https://github.com/Peter-Ufens/AI-Lab-Journal) (Peter Ufens) : tableaux clairs, peu de jargon, parcours progressif.

---

## Lis ceci en premier (si tu débutes)

Tu n’as **pas** besoin de comprendre le mot « RAG » pour commencer.

| Étape | Quoi faire | Lien |
|---|---|---|
| **0** | Comprendre l’IA en douceur (optionnel mais utile) | [Présentations Gamma — parcours découverte](https://github.com/Peter-Ufens/AI-Lab-Journal/tree/main/presentations) |
| **1** | Comprendre **ce qu’est un RAG** *sans code* | [Série RAG — 3 présentations](https://github.com/Peter-Ufens/AI-Lab-Journal/tree/main/presentations/RAG-Series) |
| **2** | Revenir ici et suivre le **parcours guidé** plus bas | ce README |

### C’est quoi un « RAG », en français simple ?

Imagine un assistant qui **ne répond pas seulement de mémoire**, mais qui **va d’abord chercher** dans *tes* notes (Obsidian) avant de te répondre.

- **Sans RAG** : l’IA invente parfois ou ignore tes documents.  
- **Avec RAG** : l’IA s’appuie sur **tes** fichiers (carnet, procédures, idées).

Tu n’as pas à retenir le sigle. Garde l’idée : **carnet bien rangé → recherche dans le carnet → réponse plus juste**.

Pour aller plus loin (toujours sans code) :  
[Les 12 architectures RAG — Partie 1 : Les Fondations](https://gamma.app/docs/Les-12-architectures-RAG-Partie-1-Les-Fondations-ofwlpca8d82qv44)  
puis [Partie 2](https://gamma.app/docs/Les-12-Architectures-RAG-Partie-2-Le-RAG-qui-Reflechit-78v3mxi39d69dhl) · [Partie 3](https://gamma.app/docs/Les-12-Architectures-RAG-Partie-3-La-Frontiere-de-lArt-hl0806r9ziirfpk)

Glossaire local : [`GLOSSAIRE.md`](GLOSSAIRE.md)

---

## En une phrase

Ce dépôt explique **comment organiser un carnet Obsidian** et, plus tard, le relier à une **recherche dans tes notes** — sans publier ta vie privée.

---

## Pour qui ?

| Profil | Comment lire |
|---|---|
| **Non technique (RH, métier)** | 1) Présentations (lien ci-dessus) si le vocabulaire IA est flou · 2) ce README jusqu’au parcours guidé · 3) coller le README dans Claude/ChatGPT : *« guide-moi étape par étape »* |
| **Technique** | Ensuite : `config.example.env`, `vault-skeleton/`, puis scripts (repo ops privé ou projet local) |
| **Assistant IA** | Voir [`POUR-ASSISTANT-IA.md`](POUR-ASSISTANT-IA.md) |

---

## Ce que ça fait / ne fait pas

| Oui | Non |
|---|---|
| Structure de dossiers pour un vault Obsidian | Tes notes personnelles |
| Une idée claire de pipeline : notes → idées → recherche | Clés API, mots de passe |
| Config exemple à adapter | Un cloud magique tout fait |
| Liens vers des présentations **vulgarisées** | Remplacer un cours IA complet |

---

## Parcours guidé (débutant) — Obsidian d’abord

Tu peux **ignorer** Ollama et le RAG au début. L’important = un carnet clair.

1. **Installer Obsidian** (application gratuite).
2. **Créer un vault vide** (un dossier sur ton PC).
3. **Reproduire les dossiers** listés dans [`vault-skeleton/STRUCTURE.txt`](vault-skeleton/STRUCTURE.txt).
4. *(Plus tard)* Installer **Ollama** si tu veux des modèles sur ton PC — voir aussi la présentation [Faire tourner une IA sur son PC](https://gamma.app/docs/Faire-tourner-une-IA-sur-son-PC-en-4-etapes-kb1cg2xuckkkr0p).
5. **Copier `config.example.env`** → `config.env` et indique le chemin de ton vault.
6. Demander à un assistant IA : *« J’ai ce README et ce config.example.env, aide-moi à remplir les chemins sur Windows. Je débute. »*

---

## Fichiers de ce template

| Fichier | Rôle |
|---|---|
| `README.md` | Tu es ici |
| `POUR-ASSISTANT-IA.md` | Consignes pour Claude / ChatGPT |
| `config.example.env` | Chemins à adapter (sans secrets) |
| `vault-skeleton/` | Arborescence recommandée |
| `GLOSSAIRE.md` | Mots techniques en français simple |

---

## Ressources sœurs (même auteur)

| Ressource | Pourquoi |
|---|---|
| [AI-Lab-Journal](https://github.com/Peter-Ufens/AI-Lab-Journal) | Hub public — journal, certifs, conventions |
| [Présentations](https://github.com/Peter-Ufens/AI-Lab-Journal/tree/main/presentations) | Index Gamma (débutants → pratique) |
| [Série RAG](https://github.com/Peter-Ufens/AI-Lab-Journal/tree/main/presentations/RAG-Series) | Comprendre le RAG **sans code** |

---

## Langue et accessibilité

- Français d’abord.
- Tableaux de statut (comme un journal de bord).
- Si un mot technique apparaît → [`GLOSSAIRE.md`](GLOSSAIRE.md) ou les présentations Gamma.
- Public = **tout le monde peut ouvrir le repo** ; le contenu privé reste hors de ce template.
