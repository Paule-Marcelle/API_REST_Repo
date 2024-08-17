# Git Worktrees

Les **git worktrees** permettent de travailler sur plusieurs branches d'un même dépôt Git sans avoir à changer de branche dans un seul répertoire de travail. Voici quelques exemples détaillés pour vous aider à comprendre et utiliser cette fonctionnalité.

## Ajouter un Worktree

Pour ajouter un nouveau worktree pour une branche appelée `feature-x`, utilisons la commande suivante :

```bash
git worktree add ../feature-x-worktree feature-x
```
'../feature-x-worktree : Le chemin vers le répertoire où le nouveau worktree sera créé.
feature-x : La branche sur laquelle nous allons travailler dans ce nouveau worktree.

# Travailler dans le Worktree
Une fois le worktree créé, vous pouvez naviguer dans le répertoire du worktree et travailler dessus comme si c'était un dépôt Git indépendant :
```bash
cd ../feature-x-worktree
# Vous pouvez maintenant travailler sur la branche feature-x
```
# Supprimer un Worktree
```bash
git worktree remove ../feature-x-worktree
#Cela supprimera le répertoire feature-x-worktree et nettoiera les références du worktree. Notons que cela n'efface pas la branche feature-x dans le dépôt principal.
```
#Listes des Worktrees
```bash
git worktree list
```
#CODE ETAPES WORKTREES
```bash

git worktree add ../feature-x-worktree feature-x

cd ../feature-x-worktree
# Faites vos modifications et commits sur feature-x

cd path/to/main-worktree
# Travaillez sur la branche main

git worktree add ../experiment-worktree experiment

cd ../experiment-worktree
# Faites vos tests et ajustements

git worktree remove ../experiment-worktree

```
