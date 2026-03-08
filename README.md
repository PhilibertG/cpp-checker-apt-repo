# 🚀 EPITECH C++ Coding Style Checker - Official Repository

Bienvenue sur le dépôt officiel du **EPITECH C++ Coding Style Checker**. Cet outil est conçu pour aider les étudiants et développeurs d'EPITECH à valider automatiquement leur code C++ selon les normes officielles de l'école.

## 🌟 Points Forts

*   **Vitesse Ultime** : Exécution parallèle utilisant tous les cœurs de votre CPU.
*   **Zéro Faux Positif** : Intégration de `clang-format` pour une mise en forme parfaite.
*   **Intelligence Sémantique** : Analyse de l'arbre syntaxique (AST) via `libclang` pour détecter les erreurs de conception (private attributes, RAII, etc.).
*   **Compatible CI/CD** : GitHub Action native disponible.

---

## 🛠 Installation

### 🐧 Debian / Ubuntu (APT)

```bash
# 1. Ajouter le dépôt
echo "deb [trusted=yes] https://philibertg.github.io/cpp-checker-apt-repo stable main" | sudo tee /etc/apt/sources.list.d/cpp-checker.list

# 2. Installer l'outil
sudo apt update
sudo apt install cpp-coding-style-checker
```

### 🎩 Fedora / RHEL / CentOS (DNF)

```bash
# 1. Ajouter le dépôt
sudo tee /etc/yum.repos.d/cpp-checker.repo << 'EOF'
[cpp-checker]
name=EPITECH C++ Coding Style Checker
baseurl=https://philibertg.github.io/cpp-checker-rpm-repo
enabled=1
gpgcheck=0
EOF

# 2. Installer l'outil
sudo dnf install cpp-coding-style-checker
```

---

## 📖 Guide d'Utilisation Complet

### 1. Analyse Standard
Pour vérifier le style de votre projet actuel :
```bash
cpp-coding-style-checker .
```

### 2. Le Mode Silencieux (`--quiet`)
Idéal pour se concentrer sur les erreurs critiques qui font échouer le projet :
```bash
cpp-coding-style-checker . --quiet
```
*   N'affiche **que** les erreurs **MAJOR**.
*   Retourne un code de succès (0) s'il n'y a que des erreurs mineures.

### 3. Liste des Règles (`--rules`)
Affiche toutes les règles supportées et leurs descriptions :
```bash
cpp-coding-style-checker . --rules
```

### 4. Exécution Parallèle (Automatique)
L'outil détecte automatiquement votre nombre de cœurs CPU et répartit la charge. Aucune configuration requise, c'est juste **beaucoup plus rapide**.

---

## 🔍 Liste des Règles Vérifiées

### 📐 Mise en Forme (Layout)
*   **L1 (Line content)** : Une seule instruction par ligne.
*   **L2 (Indentation)** : 4 espaces obligatoires (pas de tabulations).
*   **L3 (Spaces)** : Espacements corrects autour des opérateurs et mots-clés.
*   **L4 (Braces)** : Accolades à la ligne pour les fonctions, en fin de ligne pour le reste.
*   **F2 (Line length)** : Colonnes limitées à 80 caractères.

### 📛 Nommage (Naming)
*   **N2 (Files)** : Fichiers en PascalCase.
*   **N3 (Functions)** : Fonctions en camelCase.
*   **N4 (Variables)** : Variables locales en camelCase, globales en UPPERCASE.
*   **N5 (Types)** : Classes, Structures, Enums en PascalCase.

### 🏗 Conception & C++ Avancé
*   **D2 (Encapsulation)** : Attributs de classe obligatoirement privés.
*   **D5 (Constness)** : Utilisation de `const` sur les méthodes qui ne modifient pas l'objet.
*   **D6 (RAII)** : Interdiction des fonctions `init()`, utilisation obligatoire des constructeurs.
*   **G8 (C-style)** : Interdiction des fonctions globales (tout doit être dans une classe, sauf `main`).
*   **S2 (Smart Pointers)** : Utilisation de `std::unique_ptr`, interdiction de `delete` manuel.
*   **V2 (POD)** : Les `struct` ne doivent servir qu'à stocker des données (pas de méthodes).

---

## 🤖 Intégration GitHub Actions

Ajoutez simplement ceci à votre workflow pour valider chaque Push ou Pull Request :

```yaml
- name: EPITECH C++ Style Check
  uses: PhilibertG/cpp-coding-style-checker@v3
  with:
    quiet: 'true'
```

---

## 🆘 Support & Maintenance

Si vous rencontrez un problème ou souhaitez proposer une règle :
👉 [Ouvrir une Issue sur GitHub](https://github.com/PhilibertG/cpp-coding-style-checker/issues)

*Développé avec ❤️ pour la communauté EPITECH.*
