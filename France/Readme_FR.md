# Analyse Nationale des Accidents de la Route en France (2005-2023)

## 📋 Description du Projet

Cette analyse présente une étude complète des accidents de la route en France métropolitaine sur la période 2005-2023. Elle exploite les données officielles nationales pour identifier les tendances, facteurs de risque et évolutions de la sécurité routière à l'échelle du pays.

## 📊 Sources de Données

- **Données principales** : Base nationale des accidents corporels de la circulation
- **Fichiers utilisés** :
  - `caracteristiques_*.csv` : Caractéristiques générales des accidents
  - `lieux_*.csv` : Informations sur les lieux d'accidents
  - `usagers_*.csv` : Données sur les victimes et usagers
- **Période** : 2005, 2008, 2011, 2014, 2017, 2020, 2023
- **Périmètre géographique** : France métropolitaine

## 🎯 Objectifs de l'Analyse

1. **Analyser l'évolution temporelle** des accidents par type de route
2. **Étudier la répartition des victimes** par sexe et gravité des blessures
3. **Examiner l'impact de l'âge** sur la gravité des accidents
4. **Analyser les accidents selon le motif** de déplacement
5. **Identifier les tendances nationales** de sécurité routière

## 🔍 Méthodologie

### Traitement des Données

- **Nettoyage automatique** des séparateurs CSV variables selon les années
- **Géolocalisation** : Filtrage France métropolitaine (lat: 41.0-51.5°, long: -5.0-9.5°)
- **Correction GPS** : Normalisation des coordonnées mal formatées
- **Fusion multi-tables** : Jointure des fichiers caractéristiques, lieux et usagers

### Encodages et Formats

- **Gestion multi-encodage** : UTF-8 et Latin1 selon les fichiers
- **Séparateurs adaptatifs** : Détection automatique (virgule/point-virgule)
- **Années normalisées** : Conversion 2-digits → 4-digits

## 📈 Analyses Réalisées

### 1. Évolution par Type de Route (2005-2023)

**Analyse longitudinale** des accidents selon :

- Routes départementales
- Voies communales  
- Autoroutes
- Routes nationales
- Autres infrastructures

### 2. Répartition par Sexe et Gravité

**Étude démographique** des victimes :

- Répartition hommes/femmes
- Gravité : Indemne, Blessé léger, Blessé hospitalisé, Tué
- Analyse comparative des taux de mortalité

### 3. Impact de l'Âge sur la Gravité

**Segmentation par tranches d'âge** :

- 0-17 ans, 18-25 ans, 26-40 ans, 41-60 ans, 61-80 ans, 80+ ans
- Vulnérabilité selon l'âge
- Taux de mortalité par tranche

### 4. Analyse par Motif de Déplacement

**Contexte des accidents** selon le trajet :

- Domicile-travail
- Domicile-école
- Courses-achats
- Professionnel
- Loisirs
- Autre

## 🚨 Résultats Principaux

### 📊 Évolution Temporelle (2005-2023)

- **Routes départementales** : Plus accidentogènes, pic à 25 660 accidents en 2023
- **Augmentation globale** : +189,56% de 2005 à 2017, puis +93,78% de 2017 à 2023
- **Voies communales** : Forte hausse de 1 318 (2008) à 11 368 (2017)

### 👥 Répartition par Sexe

- **Hommes** : 681 878 victimes (67,35%)
- **Femmes** : 331 981 victimes (32,65%)
- **Mortalité masculine** : 3,09% vs 1,92% chez les femmes
- **Surreprésentation masculine** dans les accidents graves

### 🧓 Vulnérabilité par Âge

- **80+ ans** : Taux de mortalité le plus élevé (6,93%)
- **0-17 ans** : Majorité de blessures légères (51,37%)
- **26-60 ans** : Meilleur taux d'indemnes (45,63%)
- **Fragmentation croissante** avec l'âge

### 🚗 Motifs de Déplacement

- **Trajets professionnels** : Les plus sûrs (64,06% d'indemnes)
- **Courses-achats** : Taux de mortalité élevé (3,84%)
- **Domicile-école** : Forte proportion de blessures légères (49,37%)

## 🛠️ Technologies et Outils

- **Python** : Langage principal d'analyse
- **Pandas** : Manipulation et fusion des datasets
- **Matplotlib & Seaborn** : Visualisations statistiques
- **Gestion multi-format** : CSV avec séparateurs variables
- **Traitement géospatial** : Filtrage coordonnées GPS

## 📁 Structure des Données

```text
France/
├── test_final.ipynb         # Notebook principal d'analyse
├── Readme_FR.md            # Ce fichier
└── donnee_accident/        # Dossier des données sources
    ├── 2005/
    │   ├── caracteristiques_2005.csv
    │   ├── lieux_2005.csv
    │   └── usagers_2005.csv
    ├── 2008/ ... 2023/      # Autres années
    └── [structure similaire]
```

## 🔄 Reproductibilité

### Prérequis

- Python 3.8+
- Bibliothèques : `pandas`, `matplotlib`, `seaborn`, `glob`, `csv`

### Exécution

1. **Placer les données** dans le dossier `donnee_accident/`
2. **Respecter la structure** par année avec les 3 fichiers CSV
3. **Lancer le notebook** `test_final.ipynb`
4. **Exécuter séquentiellement** toutes les cellules

## 📝 Points Techniques

### Défis de Traitement

- **Hétérogénéité des formats** CSV selon les années
- **Gestion des encodages** multiples (UTF-8/Latin1)
- **Volumes importants** : Plus d'1 million de lignes traitées
- **Géolocalisation** : Correction des coordonnées aberrantes

### Solutions Implémentées

- **Détection automatique** des séparateurs CSV
- **Try/catch multi-encodage** pour la lecture des fichiers
- **Filtrage géographique** strict France métropolitaine
- **Normalisation** des codes temporels

## 📈 Implications et Recommandations

### Tendances Nationales

1. **Augmentation préoccupante** des accidents sur routes départementales
2. **Vulnérabilité accrue** des populations âgées (80+)
3. **Persistance des inégalités** hommes/femmes en sécurité routière
4. **Sécurité relative** des trajets professionnels

### Pistes d'Amélioration

- **Sécurisation renforcée** des routes départementales
- **Programmes ciblés** pour les seniors
- **Sensibilisation différenciée** par sexe et âge
- **Aménagements spécifiques** selon les motifs de déplacement

---
