# Analyse des Dangers Routiers à Bordeaux

## 📋 Description du Projet

Ce projet analyse les données d'accidents de la route et de trafic de Bordeaux Métropole pour identifier les zones les plus dangereuses et comprendre les facteurs de risque.

## 📊 Sources de Données

- **Données de trafic** : `comptage-du-trafic-2023-bordeaux-metropole.csv`
- **Données d'accidents** : `accidents_bordeaux_cub_2023.csv`

## 🎯 Objectifs

1. **Identifier les rues les plus dangereuses** en croisant données de trafic et d'accidents
2. **Analyser les facteurs de risque** : heure, luminosité, météo, type de collision
3. **Créer un score de dangerosité pondéré** pour prioriser les interventions

## 🔍 Méthodologie

### Score de Dangerosité

```text
Score = α × Trafic_Moyen_Journalier + β × Taux_Accidents
```

- **α = 1** : coefficient pour le volume de trafic
- **β = 1000** : coefficient pour le taux d'accidents (pour 10 000 véhicules)

### Calculs Clés

- **Trafic annuel** = Moyenne Journalière Observée × 365
- **Taux d'accidents** = (Nombre d'accidents / Trafic annuel) × 10 000

## 📈 Analyses Réalisées

### 1. Classification des Rues par Dangerosité

- Fusion des données de trafic et d'accidents par nom de voie
- Calcul du score pondéré pour chaque rue
- Classement des 10 rues les plus dangereuses

### 2. Analyse Temporelle

- **Répartition par heure** : Pics aux heures de pointe (7h-9h et 17h-20h)
- **Impact de la luminosité** : Majorité des accidents en plein jour

### 3. Analyse des Conditions

- **Météorologie** : Temps normal majoritaire, mais impact significatif de la pluie
- **Type de route** : Voies communales les plus touchées
- **Type de collision** : Accidents d'angle aux intersections prédominants

### 4. Visualisations

- Graphique en barres des rues les plus dangereuses
- Heatmap accidents par type de route × luminosité
- Histogramme des accidents par heure
- Répartitions par conditions météo et types de collision

## 🚨 Résultats Principaux

### Facteurs de Risque Identifiés

1. **Heures de pointe** : 7h-9h et 17h-20h
2. **Intersections** : Collisions d'angle fréquentes
3. **Voies communales** : Plus d'accidents que les grands axes
4. **Conditions dégradées** : Pluie et faible luminosité

### Recommandations

- Renforcer la signalisation aux intersections
- Améliorer l'éclairage des voies communales
- Sensibiliser aux distances de sécurité
- Sécuriser les passages piétons

## 🛠️ Technologies Utilisées

- **Python** pour l'analyse de données
- **Pandas** pour la manipulation des données
- **Matplotlib & Seaborn** pour les visualisations
- **Jupyter Notebook** pour l'analyse interactive

## 📁 Structure des Fichiers

```text
Bordeaux/
├── danger_bordeaux.ipynb    # Notebook principal d'analyse
├── Readme_BDX.md           # Ce fichier
├── trafic/                 # Données de comptage du trafic
└── 2023/                   # Données d'accidents 2023
```

## 🔄 Reproductibilité

Pour reproduire l'analyse :

1. Installer les dépendances : `pandas`, `matplotlib`, `seaborn`
2. Placer les fichiers CSV dans les dossiers appropriés
3. Exécuter le notebook `danger_bordeaux.ipynb`

## 📝 Notes Techniques

- Gestion des valeurs manquantes avec `fillna(0)`
- Conversion des types de données pour assurer la cohérence
- Fusion des datasets sur les noms de voies
- Normalisation des scores pour comparaison équitable

---

Analyse réalisée dans le cadre du projet de fin d'année - Bordeaux Métropole 2023
