# EPITECH C++ Coding Style Checker - APT Repository

Repository APT pour l'installation simplifiée du checker de style C++ EPITECH.

## Installation

### 1. Ajouter le repository

```bash
echo "deb [arch=amd64 trusted=yes] https://philibertg.github.io/cpp-checker-apt-repo stable main" | \
  sudo tee /etc/apt/sources.list.d/cpp-checker.list
```

### 2. Mettre à jour et installer

```bash
sudo apt update
sudo apt install cpp-coding-style-checker
```

### 3. Vérifier l'installation

```bash
cpp-coding-style-checker --help
```

## Utilisation

### Vérifier un projet

```bash
# Dans le répertoire de votre projet
cd /path/to/your/project
cpp-coding-style-checker .
```

### Voir le rapport

Le rapport est généré dans `cpp-coding-style-reports.log`:

```bash
cat cpp-coding-style-reports.log
```

### Exemple de sortie

```
═══ src/main.cpp ═══
  Line   15 │ MAJOR │ F1  │ function has 28 lines (max 25)
  Line   42 │ MINOR │ N3  │ function 'Bad_Name' should be camelCase
```

## Mise à jour

```bash
sudo apt update && sudo apt upgrade
```

## Désinstallation

```bash
sudo apt remove cpp-coding-style-checker
sudo rm /etc/apt/sources.list.d/cpp-checker.list
```

# Règles Implémentées V1.0.13

## Fonctions (F)

- **F1** [MAJOR/INFO] : Les fonctions ne doivent pas dépasser 25 lignes
  - INFO (warning) : 21-25 lignes
  - MAJOR (erreur) : > 25 lignes

## Nommage (N)

- **N3** [MINOR] : Les noms de fonctions doivent être en camelCase
  - Exception : `main` est autorisé
- **N4** [MINOR] : Les noms de variables doivent être en camelCase
  - Accepte le préfixe underscore pour les membres privés (`_memberVariable`)
  - Exception : constantes en UPPER_SNAKE_CASE

## Classes (K)

- **K2** [MINOR] : Les constructeurs doivent utiliser des listes d'initialisation
- **K3** [MINOR] : Les modificateurs d'accès doivent être ordonnés (public, protected, private)

## En-têtes (H)

- **H1** [MAJOR] : Les fichiers d'en-tête ne doivent contenir que des déclarations
- **H2** [MAJOR] : Les fichiers d'en-tête doivent avoir des gardes d'inclusion ou `#pragma once`
- **H3** [MINOR] : Préférer const/constexpr à #define pour les constantes

## Mise en Forme - Layout (L)

- **L1** [MINOR] : Une ligne doit correspondre à un seul statement
  - Pas de multiples `;` sur une ligne (sauf dans les boucles `for`)
  - Pas d'assignations multiples (`a = b = c`)
  - Pas de structure de contrôle et statement sur la même ligne (`if (...) return;`)

- **L2** [MINOR] : L'indentation doit utiliser 4 espaces
  - Pas de tabulations
  - Chaque niveau d'indentation doit être un multiple de 4 espaces

- **L3** [MINOR] : Espaces corrects autour des opérateurs et keywords
  - Espace obligatoire après les virgules
  - Espace obligatoire après les keywords (`if`, `while`, `for`, `switch`, `return`)
  - Pas d'espace entre le nom de fonction et la parenthèse ouvrante
  - Espaces autour des opérateurs binaires

- **L4** [MINOR] : Placement correct des accolades
  - Accolade ouvrante en fin de ligne pour les structures de contrôle
  - Accolade ouvrante sur nouvelle ligne pour les fonctions
  - Accolade fermante seule sur sa ligne (sauf avant `else`)

- **L5** [MINOR] : Déclaration de variables correcte
  - Une seule variable par ligne
  - Variables initialisées lors de la déclaration

- **L6** [INFO] : Sauts de ligne pour la lisibilité
  - Avertissement si trop de lignes consécutives sans espacement (>25 lignes)

## Général (G)

- **G1** [MINOR] : Les fichiers doivent contenir l'en-tête EPITECH

## Avancé (A)

- **A9** [MAJOR] : Pas de directive `using namespace` dans la portée globale

---

## Légende des Sévérités

- **MAJOR** : Erreur grave qui doit être corrigée
- **MINOR** : Problème de style qui devrait être corrigé
- **INFO** : Avertissement informatif

## Support

- **Repository**: https://github.com/philibertg/cpp-checker-apt-repo
- **Issues**: https://github.com/philibertg/cpp-checker-apt-repo/issues

Développé pour EPITECH
