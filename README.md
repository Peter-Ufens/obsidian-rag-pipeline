# Pipeline Obsidian + RAG — mode d’emploi simple

> **Public · sans données personnelles.**  
> Ton : clair, francophone, lisible pour un profil RH ou métier — et pour un assistant IA (Claude, ChatGPT) qui t’accompagne.

Inspiré du style de documentation de [AI-Lab-Journal](https://github.com/Peter-Ufens/AI-Lab-Journal) (Peter Ufens) : pragmatique, tableaux de statut, pas de jargon inutile.

---

## En une phrase

Ce dépôt explique **comment organiser un carnet Obsidian** et le relier à une **recherche intelligente locale (RAG)** — sans exposer la vie privée de quelqu’un.

---

## Pour qui ?

| Profil | Comment lire |
|---|---|
| **Non technique (RH, métier)** | Lis uniquement cette page + la section « Parcours guidé ». Tu peux coller ce README dans Claude/ChatGPT et demander : *« guide-moi étape par étape »*. |
| **Technique** | Ensuite : `config.example.env`, `vault-skeleton/`, scripts du projet parent. |
| **Assistant IA** | Voir `POUR-ASSISTANT-IA.md` — consignes pour accompagner l’humain sans inventer de chemins. |

---

## Ce que ça fait / ne fait pas

| Oui | Non |
|---|---|
| Structure de dossiers pour un vault Obsidian | Tes notes personnelles |
| Idée d’un pipeline : conversations → idées → RAG | Clés API, mots de passe |
| Config exemple à adapter | Un cloud magique tout fait |

---

## Parcours guidé (débutant)

1. **Installer Obsidian** (application gratuite).
2. **Créer un vault vide** (un dossier sur ton PC).
3. **Reproduire les dossiers** listés dans `vault-skeleton/STRUCTURE.txt`.
4. **Installer Ollama** si tu veux des modèles locaux (optionnel au début).
5. **Copier `config.example.env`** → `config.env` et indique le chemin de ton vault.
6. Demander à un assistant IA : *« J’ai ce README et ce config.example.env, aide-moi à remplir les chemins sur Windows »*.

Tu n’as pas besoin de tout comprendre le premier jour. L’important : **un seul vault**, des dossiers clairs, pas de secrets dans GitHub.

---

## Fichiers de ce template

| Fichier | Rôle |
|---|---|
| `README.md` | Tu es ici |
| `POUR-ASSISTANT-IA.md` | Prompt / consignes pour Claude ou ChatGPT |
| `config.example.env` | Chemins à adapter (sans secrets) |
| `vault-skeleton/` | Arborescence recommandée |
| `GLOSSAIRE.md` | Mots techniques en français simple |

---

## Langue et accessibilité

- Français d’abord.
- Tableaux de statut (comme un journal de bord).
- Pas de anglicismes non expliqués : s’il y en a, le glossaire les traduit.
- Public = **tout le monde peut ouvrir le repo** ; le contenu privé reste hors de ce template.
