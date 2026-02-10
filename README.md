# EPITECH C++ Coding Style Checker - APT Repository

Repository APT pour l'installation simplifiée du checker de style C++ EPITECH.

## Installation

### 1. Ajouter le repository

```bash
echo "deb [arch=amd64] https://philibertg.github.io/cpp-checker-apt-repo stable main" | \
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

## Support

- **Repository**: https://github.com/philibertg/cpp-checker-apt-repo
- **Issues**: https://github.com/philibertg/cpp-checker-apt-repo/issues

Développé pour EPITECH
