# But de ce repository

Ce repository a pour but de vous montrer les bases de GitHub Actions.
Il vous faudra le forker, et me proposer une PR dans l'exercice suivant. 
En attendant, vous pouvez regarder les PRs déjà closes, et voir les checks qui ont été exécutés.
Vous pouvez ensuite aller regarder les différents fichiers correspondant aux actions.

# Explication du code

Ce projet contient plusieurs fichiers de code Python et des workflows GitHub Actions.

1. `add2vals.py` : Il s'agit d'un outil en ligne de commande simple qui prend deux valeurs et les ajoute ensemble en utilisant la fonction 'add2' de la bibliothèque 'calc.py'.

2. `calc.py` : Cette bibliothèque contient la fonction 'add2' qui prend deux valeurs et les ajoute ensemble. Si l'une des valeurs est une chaîne de caractères, 'add2' s'assure qu'elles sont toutes deux des chaînes de caractères, ce qui donne un résultat concaténé.

3. `test_calc.py` : Ce fichier contient des tests unitaires pour la bibliothèque 'calc'. Il utilise le module 'unittest' de Python pour définir et exécuter les tests.

4. `.github/workflows/pythonapp.yml` : Ce fichier YAML définit un workflow GitHub Actions qui est déclenché lorsqu'un push ou une pull request est effectué sur la branche 'main'. Le workflow installe Python 3.8 et les dépendances du projet, puis exécute 'flake8' pour la linting et 'pytest' pour exécuter les tests unitaires.

5. `.github/workflows/label.yml` : Ce fichier YAML définit un autre workflow GitHub Actions qui est déclenché lorsqu'une pull request est créée. Il utilise l'action 'actions/labeler@v5' pour appliquer automatiquement des labels aux pull requests en fonction des fichiers modifiés.

6. `.github/labeler.yml` : Ce fichier contient la configuration pour l'action 'actions/labeler@v5'. Il définit les règles pour l'application des labels en fonction des fichiers modifiés dans une pull request.
