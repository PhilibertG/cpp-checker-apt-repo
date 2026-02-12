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

---

# Règles Implémentées V1.0.15

## Fonctions (F)

- **F1** [MAJOR/INFO] : Nombre de lignes (recommandé 20, max 25)
- **F2** [MINOR] : Nombre de colonnes dans les fonctions (max 80)
- **F3** [MAJOR] : Nombre d'arguments (max 5)
- **F4** [MINOR] : Pas de void pour les fonctions sans arguments
- **F5** [MINOR] : Pas de commentaires dans les fonctions
- **F6** [MINOR] : Polymorphisme (virtual/override/final)
- **F7** [MINOR] : Paramètres callables (std::function)
- **F8** [MINOR] : Copy elision (passage par référence)

## Nommage (N)

- **N3** [MINOR] : Noms de fonctions en camelCase
- **N4** [MINOR] : Noms de variables en camelCase

## Classes (K)

- **K2** [MINOR] : Listes d'initialisation des constructeurs
- **K3** [MINOR] : Ordre des modificateurs d'accès

## En-têtes (H)

- **H1** [MAJOR] : Contenu des fichiers d'en-tête
- **H2** [MAJOR] : Gardes d'inclusion (#pragma once interdit)
- **H3** [MINOR] : Macros (préférer const/constexpr)

## Mise en Forme - Layout (L)

- **L1** [MINOR] : Une ligne = un statement
- **L2** [MINOR] : Indentation (4 espaces, pas de tabulations)
- **L3** [MINOR] : Espaces (virgules, keywords, opérateurs)
- **L4** [MINOR] : Placement des accolades
- **L5** [MINOR] : Déclaration de variables
- **L6** [INFO] : Sauts de ligne pour la lisibilité

## Structures de Contrôle (C)

- **C1** [MAJOR] : Branchements conditionnels (max 3 branches, nesting max 2)
- **C2** [MINOR] : Expressions ternaires simples
- **C3** [MAJOR] : Pas de goto
- **C4** [MINOR] : Boucles for simples
- **C5** [INFO] : Préférer les range-based for

## Portée Globale (G)

- **G1** [MINOR] : En-tête de fichier EPITECH

## Avancé (A)

- **A9** [MAJOR] : Pas de using namespace global

---

**Total : 28 règles implémentées**

## Légende

- **MAJOR** : Erreur grave
- **MINOR** : Problème de style
- **INFO** : Avertissement

---

## Support

- **Repository**: https://github.com/philibertg/cpp-checker-apt-repo
- **Issues**: https://github.com/philibertg/cpp-checker-apt-repo/issues

Développé pour EPITECH
