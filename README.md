# Projet Data Science – Analyse et Prévision de la Consommation Énergétique

## 1. Présentation du Projet

Ce projet vise à analyser de grandes séries temporelles relatives à la consommation énergétique et aux variables associées, dans le but d’identifier des tendances, des motifs saisonniers et des anomalies. L’objectif final est de développer et d’évaluer des modèles prédictifs afin d’anticiper la demande énergétique. Le projet combine l’analyse de données issues de formats CSV et NetCDF, ainsi que la génération de prédictions sauvegardées dans un fichier dédié.

## 2. Jeux de Données Fournis

Le projet s’appuie sur plusieurs types de fichiers :

- **Fichiers CSV :**
  - `Energy_Data_20200920_20231027.csv` : Données énergétiques couvrant la période du 20 septembre 2020 au 27 octobre 2023.
  - `Energy_Data_20200920_20240118.csv` : Données énergétiques étendues jusqu’au 18 janvier 2024.
  - `predictions.csv` : Résultats des prédictions de la consommation énergétique obtenus à partir du modèle.

- **Fichiers NetCDF :**
  - `dwd_icon_eu_demand_20200920_20231027.nc` : Données de demande énergétique issues du modèle ICON (DWD) pour la période initiale.
  - `dwd_icon_eu_demand_20231027_20240108.nc` : Données complémentaires couvrant la transition de la période précédente vers janvier 2024.
  - `dwd_icon_eu_demand_20240108_20240129.nc` : Données couvrant la fin de janvier 2024, permettant d’affiner la compréhension des dynamiques récentes.
  Ces fichiers sont disponibles sur ce site web: https://ieee-dataport.org/competitions/hybrid-energy-forecasting-and-trading-competition. Il vous faut télécharger les dwd_icon_eu

- **Autres fichiers :**
  - `DataScience.html` : Version web/documentée du projet, incluant des visualisations et des explications sur les méthodes employées.
  - `DataScience.ipynb` : Notebook Jupyter complet contenant le code, l’analyse exploratoire, l’ingénierie des caractéristiques et les modèles de prévision.

## 3. Objectifs du Projet

- **Analyse Exploratoire et Prétraitement :**
  - Importer et nettoyer les données (traitement des valeurs manquantes, détection d’outliers).
  - Convertir et harmoniser les formats temporels (dates, heures) pour permettre une analyse chronologique précise.
  - Explorer les tendances, motifs saisonniers et anomalies via des visualisations (graphes linéaires, heatmaps, etc.).

- **Ingénierie des Caractéristiques :**
  - Extraire des variables temporelles (jour, mois, année, heure, etc.) à partir des horodatages.
  - Construire de nouvelles variables (moyennes mobiles, indicateurs de tendance, etc.) afin d’améliorer la performance des modèles prédictifs.

- **Modélisation et Prévision :**
  - Séparer les données en ensembles d’entraînement et de test.
  - Tester plusieurs approches de modélisation (modèles statistiques, méthodes basées sur l’apprentissage automatique et le deep learning).
  - Évaluer la performance des modèles avec des métriques telles que MAE, RMSE et R².
  - Générer des prédictions sur la demande énergétique future, lesquelles sont sauvegardées dans le fichier `predictions.csv`.

- **Intégration des Données NetCDF :**
  - Exploiter les fichiers NetCDF pour enrichir l’analyse avec des données provenant de modèles météorologiques et de prévisions de demande (données ICON du DWD).
  - Comparer et éventuellement fusionner ces informations avec les données CSV pour obtenir une vision globale et robuste du comportement énergétique.

## 4. Méthodologie

### 4.1. Prétraitement et Importation des Données
- Lecture des fichiers CSV et NetCDF à l’aide de bibliothèques telles que Pandas et xarray.
- Harmonisation des formats temporels et alignement des séries temporelles issues de différentes sources.
- Nettoyage des données (gestion des valeurs manquantes et des anomalies).

### 4.2. Analyse Exploratoire (EDA)
- Visualisation de la consommation énergétique et des variables associées à l’aide de graphiques linéaires, histogrammes, boxplots et heatmaps.
- Identification des tendances saisonnières et des cycles.
- Analyse des corrélations entre la demande énergétique et d’autres facteurs potentiels (par exemple, données météorologiques issues des fichiers NetCDF).

### 4.3. Ingénierie des Caractéristiques
- Extraction de caractéristiques temporelles (jour, semaine, mois, etc.).
- Création d’indicateurs avancés (moyennes mobiles, dérivées temporelles) pour améliorer la qualité prédictive.
- Fusion des données issues des différents formats pour enrichir le jeu de caractéristiques.

### 4.4. Modélisation Prédictive et Évaluation
- Division du jeu de données en ensembles d’entraînement et de test.
- Développement de plusieurs modèles prédictifs (modèles ARIMA, forêts aléatoires, réseaux de neurones, etc.).
- Optimisation des hyperparamètres et validation croisée.
- Évaluation des performances via des métriques adaptées (MAE, RMSE, R²).
- Génération et sauvegarde des prédictions dans `predictions.csv`.

## 5. Livrables

- **Notebook Jupyter (`DataScience.ipynb`)** : Contient l’intégralité du code, l’analyse exploratoire, l’ingénierie des caractéristiques et la modélisation.
- **Fichiers de Données** : 
  - Données historiques en CSV.
  - Données complémentaires issues des fichiers NetCDF.
- **Prédictions (`predictions.csv`)** : Résultats générés par les modèles prédictifs.
- **Documentation Web (`DataScience.html`)** : Présentation interactive et détaillée du projet.

## 6. Conclusion

Ce projet offre une approche intégrée de l’analyse et de la prévision de la demande énergétique en combinant des données historiques, des données issues de modèles météorologiques et des techniques avancées de data science. La méthodologie adoptée permet de dégager des tendances, d’identifier des anomalies et de produire des prédictions fiables, facilitant ainsi une meilleure gestion et optimisation de la consommation énergétique.

---
