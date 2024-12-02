# 🧸 Toy Store KPI Report

## 📝 Résumé du Projet
- **Contexte** : Analyse des performances d'une chaîne fictive de magasins de jouets au Mexique afin de suivre les indicateurs clés (KPI) tels que les commandes, le revenu et le profit.
- **Mission** : Créer un tableau de bord interactif permettant de visualiser les tendances des ventes et d'explorer les performances par catégorie de produits et par localisation.
- **Objectifs** :
  1. Connecter et explorer les données pour établir un modèle relationnel robuste.
  2. Développer des mesures DAX pour calculer des KPI financiers et opérationnels.
  3. Concevoir un rapport interactif avec des visualisations claires et dynamiques.

---

## 🖼 Résultat Visuel

### 1. Page Overview
[![Capture d'écran du Toy Store KPI Report - Overview](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Overview.png)](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Overview.png)

---

### 2. Détail par Magasin
[![Capture d'écran du Toy Store KPI Report - Détail par Magasin](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Store_detail.png)](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Store_detail.png)

---

### 3. Page d'Extraction
[![Capture d'écran du Toy Store KPI Report - Page d'Extraction](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Extraction.png)](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Toy%20Store%20KPI%20Report/images/Capture%20d%E2%80%99%C3%A9cran_Extraction.png)

---

## 📈 Insights Clés

### 1. Performances Globales
- **Nombre total de transactions** : 421K, reflétant une activité soutenue sur l'ensemble de l'année 2022.
- **Revenu total** : 7M €, avec des ventes particulièrement solides au 4e trimestre.
- **Profit total** : 2M €, représentant une marge de profit globale de 29,27 %.

---

### 2. Analyse des Produits
- **Catégories de produits les plus performantes** (en termes de transactions) :
  - **Jouets** (118K transactions) : Catégorie leader.
  - **Jeux (87K transactions)** et **Art & Crafts (87K transactions)** : Très populaires également.
- **Top 10 des produits** :
  - **Colorbuds** génère le revenu le plus élevé avec **1,127,428 €**, et une marge de profit exceptionnelle à **53,37 %**.
  - **Deck of Cards** et **PlayDoh Can** se distinguent également, avec des marges supérieures à **33 %**.

---

### 3. Analyse Temporelle
- Le revenu mensuel suit une **saisonnalité marquée** :
  - **Point bas** : mars 2022, avec un revenu de **0,4M €**.
  - **Pic** : décembre 2022, atteignant **0,8M €**, probablement dû aux fêtes de fin d'année.
- La **marge de profit fluctue** entre **29 % et 32 %**, atteignant son maximum au 2e trimestre.

---

### 4. Objectifs Mensuels
- **Transactions du mois courant (décembre 2022)** :
  - **48,380 transactions**, soit **+24,18 %** par rapport à l'objectif fixé à **38,959 transactions**.
- **Revenu du mois courant** :
  - **877K €**, surpassant l'objectif de **661K €** de **+32,65 %**.
- **Profit du mois courant** :
  - **246K €**, dépassant l'objectif de **193K €** avec un écart de **+27,59 %**.

---

### 5. Recommandations
- **Optimiser la stratégie marketing** pour les produits à fort potentiel comme **Colorbuds** et **Deck of Cards**.
- **Augmenter les promotions** sur les catégories en croissance, telles que **Art & Crafts** et **Jeux**.
- **Surveiller la performance** des mois creux (mars) pour identifier des opportunités de relance des ventes.

---

## 🛠️ Étapes Techniques Principales

### 1. Power Query
- **Nettoyage et Transformation des Données** :
  - Fusion des fichiers CSV (`Sales`, `Products`, `Stores`, `Calendar`) pour créer une table de faits et des dimensions.
  - Ajout de colonnes calculées dans la table **Calendar** 
  - Vérification des types de données, suppression des valeurs nulles et gestion des doublons.

---

### 2. Modélisation Relationnelle
- **Conception d’un Modèle en Étoile** :
  - Tables liées :
    - **FactSales** (table de faits).
    - **DimProducts**, **DimStores**, **DimCalendar** (tables dimensionnelles).
  - Relations définies en respectant les bonnes pratiques (1:N entre dimensions et faits).
- **Optimisation** :
  - Hiérarchie temporelle : `Début du mois > Début de la semaine > Date`.
  - Masquage des clés étrangères dans **FactSales** pour une vue rapport simplifiée.

---

### 3. Calculs & Mesures DAX
- **Colonnes Calculées** :
  - `Revenu` : `Prix x Quantité`.
  - `Profit` : `Revenu - Coût`.
- **Mesures Clés** :
  - `Total Orders` : Nombre total de transactions.
  - `Total Revenue` : Somme du revenu total.
  - `Total Profit` : Somme du profit total.
- **Mesures Avancées** :
  - Création de KPI financiers (transactions, revenu, profit) pour des objectifs mensuels.
  - Calcul des écarts par rapport aux objectifs.

---

### 4. Visualisations et Interactions
- **Pages de Rapport** :
  - **Page d'Overview** : Résumé global avec KPI clés (transactions, revenu, profit, marge).
  - **Pages par Magasin** :
    - Création de **22 pages spécifiques** pour chaque magasin avec des détails individualisés.
    - Navigation facilitée grâce à des **signets** (bookmarks) permettant de basculer entre les pages.
  - **Page d’Extraction** :
    - Tableau détaillé exportable pour l'analyse approfondie.
- **Visualisations Clés** :
  - **Cartes KPI** : Indicateurs pour le mois en cours, avec comparaison par rapport aux objectifs.
  - **Graphiques** :
    - Ligne pour la marge bénéficiaire mensuelle.
    - Barres empilées pour les transactions par catégorie de produits.
    - Jauge pour comparer le revenu au target.

---

## 📄 Fichier Power BI Principal
- **Nom** : `Toy_Store_KPI_Report.pbix`
- **Description** : Tableau de bord interactif pour suivre les KPI de ventes et explorer les tendances par produit et localisation.
- **Lien** : [Télécharger le fichier Power BI](https://drive.google.com/drive/folders/ID_GOOGLE_DRIVE)

---

## 📚 Ressources
- [Documentation Power BI](https://learn.microsoft.com/fr-fr/power-bi/)
- [Guide DAX](https://dax.guide/)
