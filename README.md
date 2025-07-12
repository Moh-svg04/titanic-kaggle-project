# 🚢 Titanic - Machine Learning from Disaster (Kaggle)

Ce projet Kaggle consiste à prédire la survie des passagers du Titanic en utilisant des modèles de machine learning.  
Il s'agit d'un **classique projet de classification supervisée**, très utilisé pour apprendre la Data Science.

---

##  Objectif

Utiliser les données disponibles (sexe, âge, classe, famille, tarif, etc.) pour prédire si un passager a survécu ou non au naufrage du Titanic.

---

##  Score obtenu

** Score public Kaggle : `0.78468`**  
Ce score dépasse la baseline (`gender_submission.csv` ≈ 0.765).

---

##  Modèle utilisé

- **Random Forest Classifier** (`sklearn`)
- Avec :
  - **n_estimators = 200**
  - **max_depth = 8**
- Évalué en validation croisée (`train_test_split` 80/20)

---

##  Feature Engineering

Voici les principales features créées pour améliorer le modèle :

| Feature        | Description                                          |
|----------------|------------------------------------------------------|
| `FamilySize`   | SibSp + Parch + 1                                    |
| `IsAlone`      | 1 si le passager est seul, sinon 0                   |
| `Title`        | Extraction du titre (`Mr`, `Mrs`, `Miss`, etc.)     |
| `Sex`          | Encodé en binaire                                    |
| `Embarked`     | Encodage one-hot                                     |

---

##  Nettoyage & Préparation

- Suppression des colonnes : `Cabin`, `Ticket`, `Name`
- Imputation des valeurs manquantes (`Age`, `Embarked`, `Fare`)
- Encodage des variables catégorielles (`Sex`, `Embarked`, `Title`)

---

##  Contenu du dépôt

| Fichier                       | Rôle                                    |
|------------------------------|-----------------------------------------|
| `titanic_notebook.ipynb`     | Notebook complet avec code + commentaires |
| `submission.csv`             | Prédictions finales envoyées à Kaggle    |
| `README.md`                  | Documentation du projet                  |

---

##  A propos

Projet réalisé dans le cadre de son apprentissage en Data Science.  

---

## Compétences mobilisées

- Pandas, Numpy, Matplotlib, Seaborn
- Feature engineering, nettoyage de données
- Modélisation supervisée avec `sklearn`
- Évaluation de modèles (accuracy, classification report)
