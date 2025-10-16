<div align="center">

# 🔓 Vigenère Cipher Decoder

[![Language: C](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Cryptography](https://img.shields.io/badge/Cryptography-Vigen%C3%A8re-red.svg)](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)
[![Algorithm](https://img.shields.io/badge/Algorithm-Frequency%20Analysis-green.svg)](https://en.wikipedia.org/wiki/Frequency_analysis)
[![License](https://img.shields.io/badge/License-Open%20Source-yellow.svg)]()

### 🌍 Language / Langue

[![English](https://img.shields.io/badge/lang-English-blue.svg)](#english) [![Français](https://img.shields.io/badge/lang-Fran%C3%A7ais-red.svg)](#français)

---

</div>

## English

### 📖 Description

**Vigenère Cipher Decoder** is an advanced cryptanalysis tool that automatically decrypts Vigenère-encrypted texts without prior knowledge of the password. Using sophisticated statistical methods including **Index of Coincidence** and **frequency analysis**, this program can crack classical polyalphabetic ciphers.

### ✨ Features

- 🔍 **Automatic Password Length Detection** - Uses Index of Coincidence statistical analysis
- 🎯 **Intelligent Password Recovery** - Employs frequency analysis on letter distributions
- ⚡ **Full Decryption** - Automatically decrypts the entire ciphertext
- 📊 **Statistical Analysis** - Implements cryptanalysis algorithms
- 🔄 **Text Normalization** - Handles uppercase/lowercase variations
- 📝 **File-Based Processing** - Reads encrypted files and outputs decrypted text

### 🧮 How It Works

The algorithm uses two main cryptanalysis techniques:

1. **Index of Coincidence (IC)**
   - Measures the probability of two randomly selected letters being identical
   - For natural language text (French/English): IC ≈ 0.065 - 0.095
   - For random text: IC ≈ 0.038
   - The program tests different key lengths until the IC matches natural language patterns

2. **Frequency Analysis**
   - Analyzes letter frequency in each subset of the ciphertext
   - Assumes 'e' is the most frequent letter (valid for French and English)
   - Determines each character of the password by comparing frequencies

### 🚀 Installation & Usage

#### Compilation

```bash
gcc vigenere_decodage.c -o vigenere_decodage
```

#### Execution

```bash
./vigenere_decodage <encrypted_file> <output_file>
```

#### Example

```bash
./vigenere_decodage text_crypte_vigenere.txt sortie.txt
```

The program will:
1. Display the Index of Coincidence for each tested key length
2. Automatically detect the password length
3. Display the recovered password
4. Save the decrypted text to the output file

### 📊 Algorithm Complexity

- **Time Complexity**: O(n × k × 26)
  - n = text length
  - k = maximum password length tested (default: 100)

- **Space Complexity**: O(n)

### 🔧 Technical Details

| Component | Description |
|-----------|-------------|
| **Language** | C (ANSI C99) |
| **Dependencies** | Standard C Library (stdio, stdlib, string, math) |
| **Input** | Text file encrypted with Vigenère cipher |
| **Output** | Decrypted plaintext file |
| **Parameters** | `IDEAL_NBR_ITER`: Max iterations (100)<br>`DEBUT_INDICE_COINCI`: Min IC (0.065)<br>`FIN_INDICE_COINCI`: Max IC (0.095) |

### 📁 Project Structure

```
VigenereDecoding/
├── vigenere_decodage.c          # Main source code
├── vigenere_decodage            # Compiled executable
├── text_crypte_vigenere.txt     # Sample encrypted text
├── sortie.txt                   # Decrypted output
├── textNormalise.txt            # Normalized text (temp)
├── fileDecouper.txt             # Sliced text analysis (temp)
└── README.md                    # This file
```

---

<div align="center">

**[⬆ Back to top](#-vigenère-cipher-decoder)**

</div>

---

## Français

### 📖 Description

**Décodeur de Chiffrement Vigenère** est un outil de cryptanalyse avancé qui déchiffre automatiquement des textes chiffrés par Vigenère sans connaissance préalable du mot de passe. En utilisant des méthodes statistiques sophistiquées incluant l'**Indice de Coïncidence** et l'**analyse fréquentielle**, ce programme peut casser les chiffrements polyalphabétiques classiques.

### ✨ Fonctionnalités

- 🔍 **Détection Automatique de la Longueur du Mot de Passe** - Utilise l'analyse statistique par Indice de Coïncidence
- 🎯 **Récupération Intelligente du Mot de Passe** - Emploie l'analyse fréquentielle sur les distributions de lettres
- ⚡ **Déchiffrement Complet** - Déchiffre automatiquement l'intégralité du texte crypté
- 📊 **Analyse Statistique** - Implémente des algorithmes de cryptanalyse
- 🔄 **Normalisation du Texte** - Gère les variations majuscules/minuscules
- 📝 **Traitement par Fichiers** - Lit les fichiers cryptés et produit le texte déchiffré

### 🧮 Principe de Fonctionnement

L'algorithme utilise deux techniques principales de cryptanalyse :

1. **Indice de Coïncidence (IC)**
   - Mesure la probabilité que deux lettres sélectionnées au hasard soient identiques
   - Pour un texte en langage naturel (français/anglais) : IC ≈ 0,065 - 0,095
   - Pour un texte aléatoire : IC ≈ 0,038
   - Le programme teste différentes longueurs de clé jusqu'à ce que l'IC corresponde aux motifs du langage naturel

2. **Analyse Fréquentielle**
   - Analyse la fréquence des lettres dans chaque sous-ensemble du texte chiffré
   - Suppose que 'e' est la lettre la plus fréquente (valide pour le français et l'anglais)
   - Détermine chaque caractère du mot de passe en comparant les fréquences

### 🚀 Installation & Utilisation

#### Compilation

```bash
gcc vigenere_decodage.c -o vigenere_decodage
```

#### Exécution

```bash
./vigenere_decodage <fichier_crypté> <fichier_sortie>
```

#### Exemple

```bash
./vigenere_decodage text_crypte_vigenere.txt sortie.txt
```

Le programme va :
1. Afficher l'Indice de Coïncidence pour chaque longueur de clé testée
2. Détecter automatiquement la longueur du mot de passe
3. Afficher le mot de passe récupéré
4. Sauvegarder le texte déchiffré dans le fichier de sortie

### 📊 Complexité de l'Algorithme

- **Complexité Temporelle** : O(n × k × 26)
  - n = longueur du texte
  - k = longueur maximale du mot de passe testée (par défaut : 100)

- **Complexité Spatiale** : O(n)

### 🔧 Détails Techniques

| Composant | Description |
|-----------|-------------|
| **Langage** | C (ANSI C99) |
| **Dépendances** | Bibliothèque Standard C (stdio, stdlib, string, math) |
| **Entrée** | Fichier texte chiffré avec le chiffrement Vigenère |
| **Sortie** | Fichier texte déchiffré |
| **Paramètres** | `IDEAL_NBR_ITER` : Itérations max (100)<br>`DEBUT_INDICE_COINCI` : IC min (0,065)<br>`FIN_INDICE_COINCI` : IC max (0,095) |

### 📁 Structure du Projet

```
VigenereDecoding/
├── vigenere_decodage.c          # Code source principal
├── vigenere_decodage            # Exécutable compilé
├── text_crypte_vigenere.txt     # Exemple de texte chiffré
├── sortie.txt                   # Sortie déchiffrée
├── textNormalise.txt            # Texte normalisé (temp)
├── fileDecouper.txt             # Analyse du texte découpé (temp)
└── README.md                    # Ce fichier
```

---

<div align="center">

**[⬆ Retour en haut](#-vigenère-cipher-decoder)**

Made with ❤️ for cryptography enthusiasts

</div>
