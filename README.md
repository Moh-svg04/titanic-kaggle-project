# 🚢 Titanic - Machine Learning from Disaster (Kaggle)

Ce projet Kaggle consiste à prédire la survie des passagers du Titanic en utilisant des modèles de machine learning.  
Il s'agit d'un **classique projet de classification supervisée**, très utilisé pour apprendre la Data Science.

---

## 🎯 Objectif

Utiliser les données disponibles (sexe, âge, classe, famille, tarif, etc.) pour prédire si un passager a survécu ou non au naufrage du Titanic.

---

## 📊 Score obtenu

**✅ Score public Kaggle : `0.78468`**  
Ce score dépasse la baseline (`gender_submission.csv` ≈ 0.765), ce qui montre la pertinence du traitement des données et du modèle utilisé.

---

## 🧪 Modèle utilisé

- **Random Forest Classifier** (`sklearn`)
- Avec :
  - **n_estimators = 200**
  - **max_depth = 8**
- Évalué en validation croisée (`train_test_split` 80/20)

---

## 🔧 Feature Engineering

Voici les principales features créées pour améliorer le modèle :

| Feature        | Description                                          |
|----------------|------------------------------------------------------|
| `FamilySize`   | SibSp + Parch + 1                                    |
| `IsAlone`      | 1 si le passager est seul, sinon 0                   |
| `Title`        | Extraction du titre (`Mr`, `Mrs`, `Miss`, etc.)     |
| `Sex`          | Encodé en binaire                                    |
| `Embarked`     | Encodage one-hot                                     |

---

## 🧼 Nettoyage & Préparation

- Suppression des colonnes : `Cabin`, `Ticket`, `Name`
- Imputation des valeurs manquantes (`Age`, `Embarked`, `Fare`)
- Encodage des variables catégorielles (`Sex`, `Embarked`, `Title`)

---

## 📁 Contenu du dépôt

| Fichier                       | Rôle                                    |
|------------------------------|-----------------------------------------|
| `titanic_notebook.ipynb`     | Notebook complet avec code + commentaires |
| `submission.csv`             | Prédictions finales envoyées à Kaggle    |
| `README.md`                  | Documentation du projet                  |

---

## 🚀 Idées d'amélioration

- Utiliser **XGBoost** ou **LightGBM**
- Créer des variables comme `Deck`, `FarePerPerson`, `AgeGroup`
- Tuning d'hyperparamètres avec `GridSearchCV`
- Validation croisée `StratifiedKFold` au lieu de simple split

---

## 📌 A propos

Projet réalisé par **Moe Gueye** dans le cadre de son apprentissage en Data Science.  
👉 Score sur Kaggle : [https://www.kaggle.com/competitions/titanic](https://www.kaggle.com/competitions/titanic)

---

## 🧠 Compétences mobilisées

- Pandas, Numpy, Matplotlib, Seaborn
- Feature engineering, nettoyage de données
- Modélisation supervisée avec `sklearn`
- Évaluation de modèles (accuracy, classification report)
