# ai-odyssey

Bienvenue dans **ai-odyssey**, un dépôt conçu comme une base de connaissances centralisée, structurée et progressive couvrant l'ensemble du parcours en **Mathématiques**, **Data Science**, **Machine Learning**, **Deep Learning** et **Culture IA**.

Ce répertoire rassemble des fiches de synthèse, des aide-mémoire techniques, des scripts démonstratifs et des références théoriques pour maîtriser la chaîne de traitement de la donnée, de ses fondements mathématiques jusqu'au déploiement de modèles.

---

## Table des Matières

- [Objectifs du Répertoire](#objectifs-du-répertoire)
- [Structure du Répertoire](#structure-du-répertoire)
- [Détail des Modules](#détail-des-modules)
  - [1. Mathématiques & Statistiques Fondamentales](#1-mathématiques--statistiques-fondamentales)
  - [2. Data Science & Écosystème Python](#2-data-science--écosystème-python)
  - [3. Machine Learning & Engineering](#3-machine-learning--engineering)
  - [4. Deep Learning, Frameworks & Culture IA](#4-deep-learning-frameworks--culture-ia)
  - [5. Lexique & Références](#5-lexique--références)
- [Exemple de Workflow Intégré](#exemple-de-workflow-intégré)
- [Sources & Références](#sources--références)

---

## Objectifs du Répertoire

- **Centralisation des Connaissances** : Regrouper en un seul endroit les concepts mathématiques essentiels, la manipulation de données avec l'écosystème Python, et les algorithmes de Machine/Deep Learning.
- **Rigueur & Pratique** : Associer formules théoriques (probabilités, statistiques inférentielles, algèbre linéaire) et implémentations concrètes en Python (`numpy`, `pandas`, `scikit-learn`, `tensorflow`).
- **Bonnes Pratiques d'Ingénierie** : Promouvoir des workflows étanches et reproductibles (Pipelines, prétraitement sans fuite de données, visualisation claire et déploiement d'applications interactives).

---

## Structure du Répertoire

```text
ai-odyssey/
│
├── Module 1 : Mathématiques & Statistiques
│   ├── maths.md                       # Fondements mathématiques généraux pour l'IA
│   ├── probabilite.md                 # Lois de probabilité, variables aléatoires, Bayes
│   ├── statistiques.md                # Statistiques descriptives, distributions, tendances
│   ├── stats_inferentielles.md        # Tests d'hypothèses, intervalles de confiance, p-value
│   ├── Fondamentaux_statistique.md    # Espérance, variance (empirique & Bessel), écart-type
│   ├── ssresidual_R2.md              # Moindres carrés résiduels (SSE) et calcul du R²
│   ├── random.md                      # Génération aléatoire, tirages et distributions
│   └── fractale.md                    # Géométrie fractale et concepts avancés
│
├── Module 2 : Data Science & Écosystème Python
│   ├── Numpy.md                       # Calcul vectoriel, tableaux multidimensionnels, broadcasting
│   ├── pandas.md                      # Manipulation de DataFrames, nettoyage, agrégations, I/O
│   ├── Matplotlib.md                  # Visualisation fondamentale, graphiques 2D/3D, customisation
│   ├── Seaborn.md                     # Visualisation statistique avancée (heatmaps, pairplots)
│   ├── Notebook Jupyter.md            # Prise en main, raccourcis et environnements interactifs
│   └── Streamlit.md                   # Déploiement d'applications Web interactives pour la Data
│
├── Module 3 : Machine Learning & Engineering
│   ├── Machine_learning.md            # Vue d'ensemble du ML, notations $X$ et $y$, metrics
│   ├── Preprocessing.md               # Encodage, Normalisation (MinMax, Standard, Robust)
│   ├── Nettoyage_de_donnee.md         # Imputation de NaNs (SimpleImputer, KNNImputer)
│   ├── Pipeline.md                    # Pipelines Scikit-Learn et ColumnTransformer
│   ├── Scikit_learn.md                # Guide d'utilisation de Scikit-Learn
│   ├── Scikit_learn_livre_Aurelien_Gerond.md # Notes de lecture "Hands-On Machine Learning"
│   ├── Logistic_regression.md         # Zoom théorique : Odds, Logit, Sigmoïde
│   └── Stat_quest.md                  # Synthèses visuelles et intuitives des algorithmes
│
├── Module 4 : Deep Learning, Frameworks & Culture IA
│   ├── TensorFlow.md                  # Framework TF2, Keras API, tf.data, tenseurs
│   ├── L'Odyssée de l'IA.pdf           # Étude historique et prospective du développement de l'IA
│   ├── 1_HOML_19.pdf                  # Extraits et compléments de référence ML/DL
│   └── livre_Machine_Learning_en_Une_Semaine.pdf # Guide d'apprentissage accéléré
│
└── Lexique & Documentation
    ├── lexique.md                     # Glossaire A-Z des termes fondamentaux
    └── README.md                      # Fichier de présentation principal
```

---

## Détail des Modules

### 1. Mathématiques & Statistiques Fondamentales
- **`maths.md` & `probabilite.md`** : Concepts clés d'algèbre et d'analyse appliqués au Machine Learning, définitions des variables aléatoires, théorèmes limites et règle de Bayes.
- **`statistiques.md` & `stats_inferentielles.md`** : Statistiques descriptives (moyenne, médiane, variance, quantiles) et inférentielles (échantillonnage, tests de Student, z-test, p-value, intervalles de confiance).
- **`Fondamentaux_statistique.md` & `ssresidual_R2.md`** : Approfondissement des formules théoriques et empiriques (espérance, correction de Bessel $n-1$) et décomposition de la variance pour le calcul du coefficient de détermination $R^2$.
- **`random.md` & `fractale.md`** : Pseudo-aléatoire, distributions de probabilité et géométrie fractale.

### 2. Data Science & Écosystème Python
- **`Numpy.md` & `pandas.md`** : Manipulation efficace de tableaux multidimensionnels et de DataFrames. Opérations de filtrage, d'agrégation (`groupby`), de fusion (`merge`/`join`) et gestion des formats de fichiers.
- **`Matplotlib.md` & `Seaborn.md`** : Création de figures claires pour l'exploration de données (EDA). Représentations de distributions, matrices de corrélation, diagrammes en boîte et courbes de tendance.
- **`Notebook Jupyter.md` & `Streamlit.md`** : Utilisation des notebooks pour le prototypage et création d'applications web interactives pour valoriser les analyses et modèles.

### 3. Machine Learning & Engineering
- **`Machine_learning.md`** : Formalisation des données ($X \in \mathbb{R}^{m \times n}$, $y \in \mathbb{R}^m$), séparation Train / Validation / Test, fonctions de coût et métriques de performance.
- **`Preprocessing.md` & `Nettoyage_de_donnee.md`** : Stratégies de traitement des données brutes : imputation de valeurs manquantes (`SimpleImputer`, `KNNImputer`), encodage catégoriel (`OneHotEncoder`, `TargetEncoder`) et mise à l'échelle (`StandardScaler`, `MinMaxScaler`, `RobustScaler`).
- **`Pipeline.md`** : Élimination du risque de fuite de données (*data leakage*) par l'assemblage de `ColumnTransformer` et `Pipeline`.
- **`Scikit_learn.md`**, **`Scikit_learn_livre_Aurelien_Gerond.md`** & **`Logistic_regression.md`** : Prise en main avancée de Scikit-Learn et décorticage mathématique de la régression logistique (Odds, Logit, Sigmoïde).

### 4. Deep Learning, Frameworks & Culture IA
- **`TensorFlow.md`** : Construction, entraînement et évaluation de réseaux de neurones avec Keras et TensorFlow 2.
- **`L'Odyssée de l'IA.pdf` & Ressources Audio/Vidéo** : Perspectives historiques, grands jalons de l'IA, débats scientifiques et visions prospectives.

### 5. Lexique & Références
- **`lexique.md`** : Glossaire alphabétique complet allant d'Accuracy et AUC jusqu'à Z-score et Zero-shot learning.

---

## Exemple de Workflow Intégré

Le dépôt préconise une approche structurée allant du traitement de données jusqu'à l'évaluation du modèle :

```python
import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.impute import SimpleImputer
from sklearn.compose import make_column_transformer, make_column_selector
from sklearn.pipeline import make_pipeline
from sklearn.linear_model import LogisticRegression

# 1. Chargement et préparation des données
# df = pd.read_csv("data.csv")
# X = df.drop(columns=["target"])
# y = df["target"]

# 2. Sélection automatique des types de colonnes
num_selector = make_column_selector(dtype_include=np.number)
cat_selector = make_column_selector(dtype_exclude=np.number)

# 3. Définition des sous-pipelines de traitement
num_pipeline = make_pipeline(
    SimpleImputer(strategy="median"),
    StandardScaler()
)

cat_pipeline = make_pipeline(
    SimpleImputer(strategy="most_frequent"),
    OneHotEncoder(handle_unknown="ignore")
)

# 4. Assemblage du préprocesseur
preprocessor = make_column_transformer(
    (num_pipeline, num_selector),
    (cat_pipeline, cat_selector)
)

# 5. Pipeline global avec modèle
full_pipeline = make_pipeline(
    preprocessor,
    LogisticRegression(max_iter=1000)
)

# 6. Optimisation des hyperparamètres
param_grid = {
    "logisticregression__C": [0.1, 1.0, 10.0],
    "logisticregression__solver": ["lbfgs", "liblinear"]
}

grid_search = GridSearchCV(full_pipeline, param_grid=param_grid, cv=5, scoring="accuracy")
# grid_search.fit(X_train, y_train)
```

---

## Sources & Références

Les ressources intégrées dans ce dépôt s'appuient sur des références académiques, littéraires et pédagogiques de premier plan :

- **Ouvrages** :
  - *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Aurélien Géron)
  - *L'Odyssée de l'IA*
- **Chaînes & Plateformes Pédagogiques** :
  - *Machine Learnia* (Guillaume Saint-Cirgue)
  - *StatQuest* (Josh Starmer)
- **Conférences & Interventions** :
  - Interventions et travaux de Yann LeCun, Ilya Sutskever, et réflexions sur les fondements de l'IA moderne.