# 📊 Fabrication de Câbles : Tableau de Bord de Production et Performance

## 📝 Résumé du Projet
- **Contexte** : Analyse des performances de production et de facturation dans une usine de fabrication de câbles pour fournir une vue d'ensemble des ventes, marges, et produits les plus performants.
- **Mission** : Créer un tableau de bord interactif permettant d’explorer les performances commerciales par client et produit, d’analyser les tendances clés, et de visualiser la composition des produits.
- **Objectifs** :
  1. Préparer et modéliser les données pour garantir des analyses précises.
  2. Développer des mesures DAX personnalisées pour calculer les indicateurs clés (ventes, marges, composition).
  3. Concevoir un tableau de bord interactif et ergonomique pour les parties prenantes.

---

## 🖼 Résultat visuel
Voici trois captures d’écran du tableau de bord final réalisé dans Power BI :

![Aperçu du tableau de bord HR Analysis](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Cable%20Manufacturing%20%3A%20Production%20%26%20Performance%20Dashboard/images/Capture%20d%E2%80%99%C3%A9cran_1.png).

![Aperçu du tableau de bord HR Analysis](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Cable%20Manufacturing%20%3A%20Production%20%26%20Performance%20Dashboard/images/Capture%20d%E2%80%99%C3%A9cran_2.png).

![Aperçu du tableau de bord HR Analysis](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/Cable%20Manufacturing%20%3A%20Production%20%26%20Performance%20Dashboard/images/Capture%20d%E2%80%99%C3%A9cran_3.png).

---

## 📂 Étapes du Projet

### 1. Préparation des données 🛠️
- **Nettoyage et transformation avec Power Query** :
  - Fusion des fichiers de facturation 2022 et 2023.
  - Création d’une colonne calculée pour la marge brute (%).
  - Suppression des colonnes inutiles et harmonisation des noms de colonnes.
- **Construction du modèle en étoile** :
  - Tables de faits et dimensions identifiées :
    - `FactFacturation`, `DimClients`, `DimProduits`, `DimMarketLine`, `DimCalendar`.
  - Relations définies entre les tables pour optimiser les performances.

### 2. Conception des visualisations 📊
- **Pages interactives** :
  - **Détails Client & Produit** :
    - Matrice affichant les ventes et marges par client ou produit.
    - Filtres : période, ligne de marché, groupe de produits, groupe de clients.
  - **Analyse Pareto** :
    - Visualisation de la règle 80/20 pour les clients et produits.
    - Exploration interactive via des slicers.
  - **Composition des Produits** :
    - Diagramme circulaire pour la composition des matériaux (cuivre, aluminium, isolant).
    - Tableau des produits classés par rentabilité.
- **Navigation intuitive** :
  - Signets permettant de basculer entre les vues "Client" et "Produit".
- **Mise en forme conditionnelle** :
  - KPI de marge avec couleurs dynamiques (vert/rouge) selon un objectif de 20 %.
  - Barres de données pour visualiser les performances des ventes.

### 3. Fonctionnalités avancées 🚀
- **DAX Formulas Personnalisées** :
  - `Ventes (€)`, `Marge (€)`, `Marge (%)`, `Poids Métal (kg)`, `Poids Non Métal (%)`, etc.
- **Création d'une table de calendrier personnalisée** :
  - Colonnes calculées pour l'année, le mois (nom et numéro), et la période (ex. 2022.01).
  - Hiérarchie temporelle pour une navigation intuitive.
- **Sécurité au Niveau des Lignes (RLS)** :
  - Restrictions sur les lignes de marché pour des utilisateurs spécifiques.
  - Masquage de certaines métriques sensibles.

---

## 📈 Insights Clés

- **Analyse Client** :
  - Les **10 principaux clients** contribuent à **78 % des ventes** totales.
  - Identification des clients à faible rentabilité grâce à la marge brute (%).
- **Analyse Produit** :
  - Les produits à base de cuivre dominent les ventes, mais leur marge est plus faible que les produits combinant cuivre et aluminium.
  - Classement des produits selon leur rentabilité et leur poids.
- **Analyse de la composition** :
  - Les câbles combinant plusieurs matériaux offrent les marges les plus élevées, mettant en lumière des opportunités d’optimisation des ventes.

---

## 🛠️ Étapes Techniques Principales
- **Power Query** :
  - Fusion de fichiers, suppression des doublons, et ajout de colonnes calculées.
- **Modèle en étoile** :
  - Construction et gestion des relations pour des calculs performants.
- **DAX Avancé** :
  - Création de mesures complexes pour les KPI et graphiques Pareto.
- **Visualisations** :
  - Slicers interactifs, signets, et mise en forme conditionnelle.

---

## 📄 Fichier Power BI Principal
- **Nom** : `Cable_Manufacturing_ Insights_ Production & Performance Dashboard.pbix`
- **Description** : Tableau de bord interactif pour explorer les performances commerciales et analyser les produits les plus rentables.
- **Lien** : [Télécharger le fichier Power BI](https://drive.google.com/drive/folders/ID_DU_DOSSIER_GOOGLE_DRIVE) 

---

## 🏆 Livrables
1. **Tableau de Bord Interactif** : "Cable_Manufacturing_ Insights_ Production & Performance Dashboard".
2. **Rapport Publié** : Hébergé sur Power BI Service avec RLS activé.
3. **Rapport Paginé** : Résumé des ventes et marges pour janvier 2023.

---

## 📚 Ressources
- [Documentation Power BI](https://learn.microsoft.com/fr-fr/power-bi/)
- [Guide DAX](https://dax.guide/)
