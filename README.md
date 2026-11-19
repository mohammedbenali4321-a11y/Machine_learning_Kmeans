# Classification Non Supervisée (Clustering K-Means) sur le Jeu de Données Iris

## Description du Projet
Ce projet explore l'application de l'algorithme de clustering **K-Means** sur le célèbre jeu de données **Iris** (`load_iris` de Scikit-learn). L'objectif principal est de regrouper les fleurs en 3 clusters distincts (correspondant aux espèces *Setosa*, *Versicolor* et *Virginica*) et d'analyser l'impact de différentes techniques de mise à l'échelle (normalisation et standardisation) sur la qualité des clusters mesurée par le **Score de Silhouette**.

---

## Méthodologie et Étapes du Notebook

1. **Chargement et Préparation des Données**
   - Extraction des caractéristiques depuis `sklearn.datasets.load_iris()` sous forme de tableau NumPy et de DataFrame Pandas (`sepal length`, `sepal width`, `petal length`, `petal width`).
   - Exploration statistique descriptive (`df.describe()`) des 150 échantillons.

2. **Modélisation de Base (Sans Normalisation)**
   - Entraînement d'un modèle `KMeans(n_clusters=3, random_state=103)` directement sur les données brutes. (random_state=103, 103 selon le nom de group IA-103 ❤️❤️🩷 \ première année 😊)
   - Attribution des labels de clusters aux observations.

3. **Prétraitement : Normalisation et Standardisation**
   - Application de **MinMaxScaler** (mise à l'échelle entre 0 et 1).
   - Application de **StandardScaler** (centrage et réduction : moyenne = 0, écart-type = 1).

4. **Évaluation et Comparaison des Performances**
   - Calcul du **Silhouette Score** (compris entre -1 et 1) pour comparer la cohésion et la séparation des clusters selon chaque approche.

---

## Résultats Obtenus

| Méthode de Prétraitement | Algorithme | Score de Silhouette |
| :--- | :---: | :---: |
| **Données brutes (Sans normalisation)** | K-Means ($k=3$) | **0.6847** |
| **Normalisation (`MinMaxScaler`)** | K-Means ($k=3$) | **0.4829** |
| **Standardisation (`StandardScaler`)** | K-Means ($k=3$) | **0.4630** |

> **Observation :** Sur ce jeu de données où toutes les variables sont déjà exprimées dans la même unité (centimètres) et où la longueur/largeur des pétales porte naturellement un pouvoir discriminant élevé, l'application de K-Means sans mise à l'échelle obtient le meilleur score de silhouette (`0.6847`).

---

## Technologies et Bibliothèques Utilisées
- **Python 3**
- **Pandas** (Manipulation et structuration des données)
- **Scikit-learn** (`load_iris`, `KMeans`, `MinMaxScaler`, `StandardScaler`, `silhouette_score`)
- **Visual Studio Code**

---

## Installation et Exécution

1. **Cloner le dépôt :**
   ```bash
   git clone <url-du-depot>
   cd <nom-du-dossier>
   ```

2. **Installer les dépendances :**
   ```bash
   pip install pandas scikit-learn jupyter
   ```

3. **Lancer le notebook :**
   ```bash
   jupyter notebook
   ```

---

## Auteur
**Mohamed BEN ALI**  
Technicien Spécialisé en Intelligence Artificielle et Analyse de Données — *CMC Rabat-Salé-Kénitra*

---

## connecte moi sur :

* **LinkeDin** :   [**Mohamed BEN ALI**](https://www.linkedin.com/in/mohamed-ben-ali-m/)  
* **GitHub**   :  [**Mohamed BEN ALI**](https://github.com/mohammedbenali4321-a11y)  
* **Kaggle**   :  [**Mohamed BEN ALI**](https://www.kaggle.com/mbaitri)
* **Roadmap**  :  [**Mohamed BEN ALI**](https://roadmap.sh/u/benalimohamed)   
