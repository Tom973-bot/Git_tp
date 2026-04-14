# Projet DevOps - Initiation Git

## 1. Description du projet
Ce projet a pour but de pratiquer les commandes de base de Git, la gestion des branches (`main` et `develop`) et la manipulation de fichiers au sein d'un dépôt GitHub.

## 2. Installation de Git
Pour installer l'outil en ligne de commande, utilisez la commande suivante selon votre système :

```bash
# Sur Debian/Ubuntu
sudo apt-get install git

# Sur macOS (avec Homebrew)
brew install git
```

# Documentation et commandes utilisées
Voici les sources officielles consultées pour ce TP :

Documentation officielle :

https://git-scm.com/docs

Se créer une connexion SSH à son Github:

https://docs.github.com/fr/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

### Tableau des commandes réalisées

| Commande | Description |
| :--- | :--- |
| `git checkout -b develop` | Crée la branche **develop** et bascule dessus. |
| `mkdir DevOps` | Crée le dossier nommé **DevOps**. |
| `touch file1 file2 file3` | Crée les fichiers vides file1, file2 et file3. |
| `git add .` | Prépare les fichiers pour le prochain commit. |
| `git commit -m "message"` | Enregistre les changements dans l'historique. |
| `git push origin develop` | Envoie les modifications sur GitHub. |
| `git merge develop` | Fusionne la branche develop sur la branche main. |
| `git mv file1 file1.txt` | Renomme le fichier file1 en file1.txt. |
| `git rm file3` | Supprime le fichier file


# Diagramme du flow de Git

```mermaid
gitGraph
    commit id: "Initial commit (main)"
    branch develop
    checkout develop
    commit id: "Création file1, 2, 3"
    checkout main
    merge develop id: "Premier Merge"
    checkout develop
    commit id: "Renommer file1 & Supprimer file3"
    checkout main
    merge develop id: "Merge final"
