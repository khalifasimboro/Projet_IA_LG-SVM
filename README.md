# Classification Binaire des Échantillons (Cancer du Côlon)

Ce projet utilise des techniques de Machine Learning pour classifier des échantillons de gènes de cancer du côlon en deux catégories : *normal* et *tumoral*. Il met en œuvre deux algorithmes de classification : la **régression logistique** et la **SVM (Support Vector Machine)**. L'objectif est de comparer les performances de ces deux modèles et d'identifier les gènes les plus influents dans la prédiction du cancer du côlon.

## Table des matières
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Structure du projet](#structure-du-projet)
- [Algorithmes utilisés](#algorithmes-utilisés)
- [Résultats](#résultats)
- [Conclusion](#conclusion)
- [Auteurs](#auteurs)

## Introduction
Le projet vise à classer les échantillons de gènes associés au cancer du côlon en deux catégories, *normal* et *tumoral*. Pour ce faire, deux algorithmes de machine learning supervisé ont été utilisés : la **régression logistique** et la **SVM**. Une évaluation des performances des deux modèles a été réalisée, en analysant des métriques telles que l'accuracy, le recall, le F1-score, et la matrice de confusion.

## Dataset
Le dataset utilisé provient d'un fichier CSV contenant des échantillons de gènes du cancer du côlon. Chaque ligne représente un échantillon, avec une étiquette associée indiquant s'il est *normal* ou *tumoral*.

- **Colonnes principales :**
  - `tissue_status` : Étiquette (0 pour *normal*, 1 pour *tumoral*).
  - `id_sample` : Identifiant unique de l'échantillon (supprimé pour l'analyse).
  - **Plusieurs colonnes correspondant aux niveaux d'expression des gènes.**

- **Lien vers le dataset** : [Colon Cancer Dataset](./colon_cancer.csv)

## Installation

### Prérequis
- Python 3.x
- Jupyter Notebook ou Google Colab
- Librairies nécessaires : `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

### Installation des dépendances
```bash
pip install -r requirements.txt
```

## Structure du projet
- `colon_cancer.csv` : Le dataset utilisé.
- `SR_ECC_LR-SVM_TP.ipynb` : Le notebook contenant le code complet du projet.
- `README.md` : Fichier d'information (celui-ci).

## Algorithmes utilisés

### 1. **Régression Logistique**
La régression logistique est un modèle de classification qui prédit la probabilité d'une instance d'appartenir à une classe donnée. Dans ce projet, elle est utilisée pour prédire si un échantillon est *normal* ou *tumoral* en fonction de l'expression de gènes.

### 2. **SVM (Support Vector Machine)**
Le SVM est un modèle de classification qui sépare les données en maximisant la marge entre les différentes classes. Ici, une SVM linéaire a été utilisée pour classer les échantillons.

### 3. **Autres Algorithmes (en option)**
Le projet inclut également une étude exploratoire de modèles tels que le k-NN (k-Nearest Neighbors), les arbres de décision et la forêt aléatoire pour voir leurs performances.

## Résultats
Les deux modèles ont été évalués sur des métriques clés :

- **Régression Logistique** :
  - Accuracy (Test): `0.9317`
  - F1-Score: `0.92`
  - Matrice de confusion

- **SVM** :
  - Accuracy (Test): `0.9255`
  - F1-Score: `0.91`
  - Matrice de confusion

### Visualisation
- **Heatmap** de la matrice de corrélation pour analyser les relations entre les gènes.
- **Boxplots** et **histogrammes** pour la distribution des valeurs et la détection des outliers.
- **Barplots** des coefficients de régression logistique et SVM pour identifier les gènes les plus influents.

## Conclusion
Les résultats montrent que la **régression logistique** a légèrement surpassé la **SVM** en termes de précision et de F1-score, notamment en utilisant les **top 3 gènes** les plus influents pour les prédictions. Cependant, les deux modèles montrent des performances similaires et solides pour cette tâche de classification binaire.

### Principaux points :
- **Régression logistique** : Plus performante pour l'équilibre des classes.
- **SVM** : Performances comparables mais légèrement inférieures en précision.

## Auteurs
- **Rydouane Simboro** – [LinkedIn](www.linkedin.com/in/rydouane-simboro-224b222a3)
