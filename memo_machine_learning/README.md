# memo-machine_learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00.svg)](https://www.tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](#)

Bienvenue dans **memo-machine_learning**, un **aide-mémoire synthétique, structuré et illustré** couvrant l'ensemble de la chaîne de valeur du **Machine Learning** et du **Deep Learning** en Python. 

Ce repo regroupe des notes, des fiches mathématiques, des synthèses théoriques et des extraits de code prêts à l'emploi inspirés des meilleures ressources pédagogiques (*Machine Learnia*, *StatQuest*, *Hands-On Machine Learning* d'Aurélien Géron).

---

## Table des Matières

- [Objectifs du Répertoire](#-objectifs-du-répertoire)
- [Structure des Fichiers](#-structure-des-fichiers)
- [DÉTAIL DES MODULES](#-détail-des-modules)
  - [1. Fondations & Théorie](#1-fondations--théorie)
  - [2. Prétraitement & Nettoyage de Données](#2-prétraitement--nettoyage-de-données)
  - [3. Pipelines & Moteur Scikit-Learn](#3-pipelines--moteur-scikit-learn)
  - [4. Modèles Fares & Zooms Algorithmiques](#4-modèles-fares--zooms-algorithmiques)
  - [5. Deep Learning & Frameworks](#5-deep-learning--frameworks)
  - [6. Lexique & Glossaire](#6-lexique--glossaire)
- [Exemples de Code & Workflow Type](#-exemples-de-code--workflow-type)
- [Références & Sources](#-références--sources)

---

## Objectifs du Répertoire

- **Aide-mémoire rapide** : Retrouver en quelques secondes une formule mathématique ($R^2$, logit, sigmoïde, matrice de confusion) ou une syntaxe Scikit-Learn/TensorFlow.
- **Workflow End-to-End** : Comprendre et appliquer les étapes clés d'un projet ML : exploration $\rightarrow$ nettoyage $\rightarrow$ encodage/scaling $\rightarrow$ modélisation $\rightarrow$ évaluation.
- **Bonnes pratiques** : Éviter les erreurs courantes comme la **fuite de données** (*data leakage*) grâce à l'utilisation systématique des `Pipeline` et `ColumnTransformer`.

---

## Structure des Fichiers

```text
memo-machine_learning/
│
├── Machine_learning.md               # Vue d'ensemble du ML, notation matricielle, metrics
├── Fondamentaux_statistique.md        # Espérance, variance (empirique & Bessel), écart-type
├── ssresidual_R2.md                  # Moindres carrés (SSE/RSS) et calcul détaillé du R²
├── Stat_quest.md                     # Synthèse visual/intuitive issue de StatQuest
│
├── Preprocessing.md                  # Encodage (One-Hot, Target), Scaling, Feature Eng.
├── Nettoyage_de_donnee.md            # Handling des NaNs (SimpleImputer, KNNImputer, etc.)
├── Pipeline.md                       # Pipelining avancé (make_column_transformer, Union)
│
├── Scikit_learn.md                   # Guide pratique Scikit-Learn (API, Fit/Predict/Score)
├── Scikit_learn_livre_Aurelien_Gerond.md # Notes tirées du livre "Hands-on Machine Learning"
├── Logistic_regression.md            # Zoom théorique : Odds, Logit, Sigmoïde, Frontière
│
├── TensorFlow.md                     # Intro à TF2, Keras API, tf.data, calcul distribué
└── lexique.md                        # Glossaire A-Z des termes fondamentaux du ML/DL
```

---

## DÉTAIL DES MODULES

### 1. Fondations & Théorie
- **`Machine_learning.md`** : Définition de la matrice de features $X$ ($m \times n$) et de la cible $y$ ($m \times 1$). Structure des sous-ensembles (Train / Validation / Test), fonctions de coût (MSE, MAE, Log Loss) et principe de la descente de gradient.
- **`Fondamentaux_statistique.md`** : Briques statistiques fondamentales. Formules théoriques et empiriques de l'Espérance $E(X)$, de la Variance $Var(X)$ avec correction de Bessel ($n-1$) pour échantillons, et de l'Écart-type $\sigma$.
- **`ssresidual_R2.md`** : Explication géométrique des moindres carrés résiduels (SSE/RSS). Calcul du coefficient de détermination $R^2 = 1 - \frac{SS(fit)}{SS(mean)}$, mesurant la part de variance expliquée.
- **`Stat_quest.md`** : Approche visuelle pour la comparaison des modèles, la validation croisée K-Fold, l'analyse des courbes ROC, l'AUC et l'arbitrage sensibilité/spécificité.

### 2. Prétraitement & Nettoyage de Données
- **`Preprocessing.md`** : 
  - **Encodage** : Ordinal, One-Hot, Target-Based Encoding (avec gestion du risque de data leakage via CV).
  - **Normalisation / Scaling** : `MinMaxScaler` $[0, 1]$, `StandardScaler` ($\mu=0, \sigma=1$), `RobustScaler` (médiane/IQR contre les outliers).
  - **Discrétisation & Polynômes** : `Binarizer`, `KBinsDiscretizer`, `PolynomialFeatures`.
- **`Nettoyage_de_donnee.md`** : Stratégies avancées d'imputation de données manquantes : `SimpleImputer` (mean, median, most_frequent), `KNNImputer` (voisins proches) et `MissingIndicator` (l'absence de donnée comme feature explicative).

### 3. Pipelines & Moteur Scikit-Learn
- **`Pipeline.md`** : Construction d'architectures de prétraitement étanches avec `make_pipeline`, `make_column_transformer` et `make_column_selector` (séparation automatique des colonnes numériques et catégorielles).
- **`Scikit_learn.md`** & **`Scikit_learn_livre_Aurelien_Gerond.md`** : Compréhension du fonctionnement des estimateurs, transformers et prédicteurs. Utilisation de `GridSearchCV` pour l'optimisation des hyperparamètres et `learning_curve` pour diagnostiquer sur/sous-apprentissage.

### 4. Modèles Phares & Zooms Algorithmiques
- **`Logistic_regression.md`** : Décorticage mathématique de la classification binaire. Passage des probabilités $p \in [0, 1]$ aux cotes (*Odds*), puis au *logit* ($\log(\text{odds}) \in ]-\infty, +\infty[$), et retour aux probabilités via la fonction Sigmoïde $\sigma(z) = \frac{1}{1 + e^{-z}}$.

### 5. Deep Learning & Frameworks
- **`TensorFlow.md`** : Présentation du framework développé par Google. API haut niveau `tf.keras`, préparation efficace des données avec `tf.data`, concepts de tenseurs et graphes de calcul distribués.

### 6. Lexique & Glossaire
- **`lexique.md`** : Répertoire alphabétique complet de **A** (Accuracy, AUC, ARIMA) à **Z** (Z-score, Zero-shot learning), couvrant les algorithmes (Random Forest, SVM, XGBoost, PCA, t-SNE) et les métriques de performance.

---

## Exemples de Code & Workflow Type

Voici un aperçu de la philosophie du repo : fabriquer des pipelines propres, lisibles et performants.

```python
import numpy as np
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.impute import SimpleImputer
from sklearn.compose import make_column_transformer, make_column_selector
from sklearn.pipeline import make_pipeline
from sklearn.linear_model import SGDClassifier

# 1. Séparation des caractéristiques et sélection automatique
X_num_selector = make_column_selector(dtype_include=np.number)
X_cat_selector = make_column_selector(dtype_exclude=np.number)

# 2. Pipelines de prétraitement dédiés
num_pipeline = make_pipeline(
    SimpleImputer(strategy='median'),
    StandardScaler()
)

cat_pipeline = make_pipeline(
    SimpleImputer(strategy='most_frequent'),
    OneHotEncoder(handle_unknown='ignore')
)

# 3. Assemblage global
preprocessor = make_column_transformer(
    (num_pipeline, X_num_selector),
    (cat_pipeline, X_cat_selector)
)

full_pipeline = make_pipeline(preprocessor, SGDClassifier(random_state=42))

# 4. Optimisation par recherche sur grille
param_grid = {
    'sgdclassifier__penalty': ['l1', 'l2', 'elasticnet'],
    'sgdclassifier__alpha': [1e-4, 1e-3, 1e-2]
}

grid_search = GridSearchCV(full_pipeline, param_grid=param_grid, cv=5, scoring='accuracy')
# grid_search.fit(X_train, y_train)
```

---

## Références & Sources

Les fiches de ce dépôt s'appuient sur des contenus de référence reconnus dans la communauté Data Science :
- **[Machine Learnia (Guillaume Saint-Cirgue)](https://www.machinelearnia.com/)** – Cours Python & Machine Learning
- **[StatQuest with Josh Starmer](https://statquest.org/)** – Explications visuelles et statistiques
- **"Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow"** par Aurélien Géron (Éditions Dunod / O'Reilly)


