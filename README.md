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

# Règles EPITECH C++ Coding Style v2.0.0

## D - Design

❌ - **D1** [MINOR] : Single Responsibility Principle
❌ - **D2** [MAJOR] : Open/closed principle
❌ - **D3** [MINOR] : Liskov Substitution Principle
❌ - **D4** [MINOR] : Dependency Inversion Principle
❌ - **D5** [MINOR] : Constness
❌ - **D6** [MINOR] : RAII

## N - Naming

❌ - **N1** [MAJOR] : General (meaningful, English)
✅ - **N2** [MAJOR] : Files and folders (PascalCase)
✅ - **N3** [MAJOR] : Functions (camelCase)
✅ - **N4** [MAJOR] : Variables (camelCase, UPPER_CASE for macros, global constants and content of enums)
✅ - **N5** [MAJOR] : Types (PascalCase)

## O - File organization

✅ - **O1** [MAJOR] : Contents of turn-in directory
✅ - **O2** [MINOR] : File extensions
❌ - **O3** [MAJOR] : File coherence

## G - Global scope

✅ - **G1** [MAJOR] : File header
✅ - **G2** [MINOR] : Separation of functions
✅ - **G3** [MINOR] : Indentation of pre-processor directives
✅ - **G4** [MAJOR] : Global variables
❌ - **G5** [MINOR] : Static
❌ - **G6** [MINOR] : Constants
✅ - **G7** [MINOR] : Template parameters
❌ - **G8** [MAJOR] : Plain C functions

## F - Functions

✅ - **F1** [MAJOR/INFO] : Number of lines (recommandé 20, max 25)
✅ - **F2** [MAJOR] : Number of columns (max 80)
✅ - **F3** [MAJOR] : Argument count (max 5)
✅ - **F4** [MINOR] : No arguments (pas de void)
✅ - **F5** [MINOR] : Comments inside function
✅ - **F6** [MINOR] : Polymorphism (virtual/override/final)
✅ - **F7** [MINOR] : Callable parameters (std::function)
✅ - **F8** [MINOR] : Copy elision (passage par référence)

## L - Layout inside a function scope

✅ - **L1** [MAJOR] : Code line content (une ligne = un statement)
✅ - **L2** [MINOR] : Indentation (4 espaces, pas de tabs)
✅ - **L3** [MINOR] : Spaces (virgules, keywords, opérateurs)
✅ - **L4** [MINOR] : Curly brackets
✅ - **L5** [MINOR] : Variable declaration
✅ - **L6** [INFO] : Line jumps

## C - Control structures

✅ - **C1** [MAJOR] : Conditional branching (max 3 branches, nesting max 2)
✅ - **C2** [MINOR] : Ternary expressions
✅ - **C3** [MAJOR] : Goto
✅ - **C4** [MINOR] : For condition and iteration expressions
✅ - **C5** [INFO] : Ranges

## V - Variables and types

✅ - **V1** [MINOR] : Pointers and references
❌ - **V2** [MINOR] : Plain Old Data Types

## K - Classes

❌ - **K1** [MAJOR] : Naming attributes
✅ - **K2** [MINOR] : Constructor list
✅ - **K3** [MINOR] : Class access modifiers
✅ - **K4** [MINOR] : Friend
❌ - **K5** [MINOR] : Operator overloads
✅ - **K6** [INFO] : Type aliases

## H - Header files

✅ - **H1** [MAJOR] : Content
✅ - **H2** [MAJOR] : Include guard (#pragma once interdit)
✅ - **H3** [MINOR] : Macros

## S - STL

❌ - **S1** [INFO] : Containers
❌ - **S2** [MINOR] : Smart pointers
❌ - **S3** [INFO] : Algorithms

## E - Error handling

✅ - **E1** [MAJOR] : Exit
❌ - **E2** [MINOR] : Return value
❌ - **E3** [MINOR] : Exceptions
❌ - **E4** [MINOR] : Exception types
❌ - **E5** [INFO] : Noexcept
✅ - **E6** [MINOR] : Return points

## A - Advanced

❌ - **A1** [MINOR] : Constant pointers
❌ - **A2** [INFO] : Scalar typing
✅ - **A3** [INFO] : NULL
❌ - **A4** [INFO] : Auto
✅ - **A5** [MINOR] : Casts
❌ - **A6** [MINOR] : C libraries
❌ - **A7** [MINOR] : Encapsulation
✅ - **A8** [INFO] : Conditional specialization
✅ - **A9** [MAJOR] : using namespace

---

## 📊 Statistiques

- **Total règles PDF** : 68 règles
- **Implémentées** : 46 règles (68%)

## 🏷️ Légende

- **MAJOR** : Erreur grave
- **MINOR** : Problème de style
- **INFO** : Avertissement

---

## Support

- **Repository**: https://github.com/philibertg/cpp-checker-apt-repo
- **Issues**: https://github.com/philibertg/cpp-checker-apt-repo/issues

Développé pour EPITECH
