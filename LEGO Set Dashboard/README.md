# 🧱 LEGO Set Explorer

## 📝 Résumé du Projet
- **Contexte** : Exploration des données des sets LEGO publiés entre 1970 et 2022 pour aider les utilisateurs à trouver le set idéal.
- **Mission** : Construire un tableau de bord interactif permettant de filtrer, analyser et explorer les données des sets LEGO en fonction de critères comme le prix, l'âge et les pièces.
- **Objectifs** :
  1. Préparer et nettoyer les données pour créer un modèle relationnel précis.
  2. Créer des colonnes calculées et des mesures DAX pour des analyses approfondies.
  3. Concevoir un rapport interactif avec des slicers, des bookmarks et des pages dynamiques.

---

## 🖼 Résultat Visuel

### 1. Page Principale
![Capture d'écran LEGO Set Explorer - Page Principale](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/LEGO%20Set%20Dashboard/images/Capture%20d%E2%80%99%C3%A9cran%20_1_dashboard.png)

---

### 2. Arbre de Décomposition
![Capture d'écran LEGO Set Explorer - Arbre de Décomposition](https://github.com/Arnaudl44/PowerBI-Projects/blob/main/LEGO%20Set%20Dashboard/images/Capture%20d%E2%80%99%C3%A9cran_2_dashboard.png).

---

## 📈 Insights Clés

### 1. Performances des Sets
- **Nombre total de sets analysés** : 18 459.
- **Plage de prix** : $1 à $850.
- **Nombre moyen de pièces** : ~400 pièces par set.

---

### 2. Analyse par Catégories
- **Groupes les plus populaires** :
  - Star Wars : Dominant en termes de pièces et de prix.
  - Technic : Sets avancés, orientés adultes.
- **Plage d'âge** : La majorité des sets sont destinés aux 5-17 ans, mais de plus en plus de produits "Over 18" apparaissent.

---

### 3. Analyse Temporelle
- Le prix moyen des sets a augmenté au fil des années, corrélé à l'augmentation des pièces.
- Les années 2020 ont vu une forte hausse de sets destinés aux adultes.

---

## 🛠️ Étapes Techniques Principales

### 1. Préparation des Données
- **Actions réalisées** :
  - Suppression des colonnes inutiles : `minifigs`, `bricksetURL`, `thumbnailURL`.
  - Filtrage des valeurs nulles pour les colonnes `price`, `age`, `pieces`, `image URL`.
  - Ajout de colonnes calculées :
    - `Age Range` : Catégories d'âge ("Over 18", "10 to 17", etc.).
    - `Price Range` : Catégories de prix ("$$$$$", "$$$", etc.).

---

### 2. Calculs & Mesures DAX
- **Mesures Créées** :
  - `Total Sets` : Nombre total de sets uniques.
  - `Total Groups` : Nombre de groupes de thèmes.
  - `Avg. Age`, `Avg. Price`, `Avg. Pieces` : Moyennes calculées pour les sets.

---

### 3. Visualisations
- **Page Principale** :
  - Cartes pour les KPIs (`Total Sets`, `Avg. Pieces`, `Avg. Price`).
  - Slicers pour filtrer par thèmes, âge et prix.
  - Tableau récapitulatif des sets avec colonnes clés.
- **Page Arbre de Décomposition** :
  - Exploration interactive du nombre total de sets (`Total Sets`) par catégories, groupes, thèmes et noms.
  - Boutons de navigation entre pages.

---

## 📄 Fichier Power BI Principal
- **Nom** : `LEGO_Set_Explorer.pbix`
- **Description** : Rapport interactif pour explorer et filtrer les sets LEGO en fonction de critères multiples.
- **Lien** : [Télécharger le fichier Power BI](https://drive.google.com/file/d/1IohN2Qd-EZ1PAFV65L4zmvUCO2anjlNB/view?usp=sharing)

---

## 📚 Ressources
- [Documentation Power BI](https://learn.microsoft.com/fr-fr/power-bi/)

---

