# Prédiction des prix immobiliers

## 📌 Description du Projet
Ce projet vise à prédire le prix des biens immobiliers (maisons/appartements) en utilisant :
- **Données géographiques**
- **Caractéristiques du bien** (surface, nombre de pièces, etc.)
- **Modèle avancé** : Gradient Boosting avec optimisation des hyperparamètres

**Approche technique** :
- Transformation log de la variable cible (prix)
- Feature engineering et prétraitement des données
- Comparaison de plusieurs modèles (Random Forest, SVR, Régression Linéaire)
- Optimisation via GridSearchCV

## 📂 Structure des Fichiers

├── data/

│ └── appartements-data.csv # Données brutes

├── notebooks/

│ ├── estimation_immobiliere.ipynb # Analyse exploratoire (EDA)

│ ├── estimation_immobiliere-GradientBoosting.ipynb # Modèle final

│ ├── estimation_immobiliere-Linear_regression.ipynb # Modèle comparatif

│ ├── estimation_immobiliere-Forest.ipynb # Modèle comparatif

│ └── estimation_immobiliere-SVR.ipynb # Modèle comparatif

│ └── Test_modele.ipynb # Permet de tester notre Modèle

├── model/

│ └── model.pkl # Modèle sauvegardé (Gradient Boosting)

└── README.md

  - Jira: https://sarabouabid.atlassian.net/jira/software/projects/MFLP/boards/34
 
 ## 🛠️ Technologies Utilisées
- **Langage**: Python, SQL
- **Librairies principales**:
  - `pandas`, `numpy` (traitement des données)
  - `scikit-learn` (modèles de ML)
  - `matplotlib`, `seaborn` (visualisation)


  📝 Méthodologie
- **Prétraitement** 
  - Nettoyage des valeurs aberrantes
  - Encodage des variables catégorielles
  - Normalisation des données numériques

- **Feature Engineering**
  - Création de variables composites (ex: prix moyen/m² par ville)
  - Sélection de features via importance des variables

- **Optimisation**
  - Validation croisée (3 folds)
  - Recherche d'hyperparamètres pour le Gradient Boosting à l'aide de GridSearchCV


  ## 🚀 Résultats Clés
### Performance des Modèles sur le jeu test (Comparaison)
| Modèle               | MAE     | R²    |
|----------------------|-------  |-------|
| **Gradient Boosting**| 273003  | 0.628 |
| Random Forest        | 341053  | 0.403 |
| SVR                  | 345829  | 0.408 |
| Régression Linéaire  | 1092424 | -2.101|
