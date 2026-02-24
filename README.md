# ⚽ Prédiction de la valeur marchande des joueurs de football

> Modèle de machine learning pour prédire la valeur marchande des joueurs de football professionnels à partir de leurs statistiques FIFA et données Transfermarkt.

---

## 🎯 Objectif

Les clubs de football dépensent des milliards chaque année sur le marché des transferts. Ce projet vise à construire un modèle prédictif fiable pour **estimer la valeur marchande d'un joueur** en 2024 à partir de ses caractéristiques sportives, physiques et de carrière.

---

## 📦 Données

| Source | Période | Variables clés |
|---|---|---|
| **FIFA** (EA Sports) | 2015 – 2024 | Overall, Pace, Shooting, Passing, Dribbling, Age |
| **Transfermarkt** | 2015 – 2024 | Valeur marchande, club, nationalité |

- ~**10 000+ joueurs** sur 10 saisons
- Fusion des deux datasets sur nom + saison

---

## 🔬 Méthodologie

```
Données brutes → Nettoyage → Feature Engineering → Modélisation → Évaluation
```

### 1. Prétraitement
- Gestion des valeurs manquantes (imputation médiane / mode)
- Encodage des variables catégorielles (OneHotEncoding, LabelEncoding)
- Normalisation et standardisation des features numériques
- Création de nouvelles features : ratio âge/overall, progression de valeur, etc.

### 2. Analyse exploratoire (EDA)
- Distribution des valeurs marchandes (loi log-normale)
- Corrélations entre attributs FIFA et valeur réelle
- Évolution des top joueurs sur 10 ans

### 3. Modélisation
- Modèle principal : **Random Forest Regressor**
- Validation croisée (k=5)
- Optimisation des hyperparamètres (GridSearchCV)

---

## 📊 Résultats

| Métrique | Score |
|---|---|
| R² Score | ~0.85 |
| MAE | ~2.1M€ |

> Les features les plus importantes : `Overall`, `Age`, `Potential`, `Club tier`, `Nationality`

---

## 🚀 Lancer le projet

```bash
# Cloner le repo
git clone https://github.com/taibi1995/Prediction-valeur-joueurs-football.git
cd Prediction-valeur-joueurs-football

# Installer les dépendances
pip install -r requirements.txt

# Lancer le notebook principal
jupyter notebook notebooks/prediction_valeur.ipynb
```

---

## 🛠️ Technologies

`Python` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

---

## 👤 Auteur

**Younes Taibi** — [LinkedIn](https://www.linkedin.com/in/younes-taibi-47690a23a/) · [GitHub](https://github.com/taibi1995)
