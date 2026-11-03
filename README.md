# 🔍 Moteur de Recherche Documentaire avec NLP et OCR

## 📝 Description
Ce projet est un moteur de recherche miniature développé en Python (sur Google Colab). Il permet d'indexer un ensemble de documents texte et de faire des recherches en utilisant deux approches : le **Modèle Vectoriel** (TF-IDF et Similarité Cosinus) et le **Modèle Booléen**. Il intègre également un module d'évaluation et une fonctionnalité **OCR** pour extraire du texte à partir d'images.

## 🚀 Fonctionnalités Principales
* **Traitement du Langage Naturel (NLP) :** Nettoyage du texte (suppression des accents), filtrage des stop-words et lemmatisation (simplification des mots).
* **Indexation :** Création d'un index inversé global sauvegardé automatiquement sous format `.json`.
* **Recherche Vectorielle :** Calcul des scores de pertinence via TF-IDF et la Similarité Cosinus pour classer les documents.
* **Recherche Booléenne :** Recherche logique stricte utilisant les opérateurs `AND`, `OR`, `NOT`.
* **Évaluation des Performances :** Calcul de la *Précision* et du *Rappel* avec génération d'une courbe d'évaluation (courbe Precision/Recall).
* **Reconnaissance Optique de Caractères (OCR) :** Extraction et nettoyage de texte depuis des images en utilisant Tesseract.

## 🛠️ Technologies et Outils
* **Langage :** Python (Google Colab)
* **Bibliothèques Standard :** `re`, `os`, `json`, `math`, `collections`, `unicodedata`
* **Visualisation :** `matplotlib`
* **OCR et Traitement d'images :** `pytesseract`, `Pillow (PIL)`, `Tesseract-OCR`

## 📂 Prérequis
Pour exécuter ce projet correctement sur Google Colab, votre Google Drive doit contenir :
1. Un dossier `/content/drive/MyDrive/projet/` contenant les fichiers textes (`.txt`) qui forment votre corpus.
2. Une image `/content/drive/MyDrive/image.png` pour tester le module OCR.

## ⚙️ Installation et Utilisation
1. Ouvrez le fichier `.ipynb` dans Google Colab.
2. Exécutez la première cellule pour monter votre Google Drive (`drive.mount`).
3. Pour la partie OCR, assurez-vous d'exécuter la cellule d'installation des dépendances :
   ```bash
   !apt-get update
   !apt-get install -y tesseract-ocr tesseract-ocr-fra
   !pip install pytesseract pillow
