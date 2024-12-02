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

## 📂 Étapes du Projet

### 1. Connexion et Exploration des Données 🔍
- **Source des Données** :
  - **Sales** : Transactions de vente.
  - **Products** : Informations sur les produits.
  - **Stores** : Localisations des magasins.
  - **Calendar** : Table calendrier.
- **Profilage des Données** :
  - Nombre de transactions enregistrées : **829,263**.
  - Nombre de magasins opérés par Maven Toys : **19**.
  - Gamme de prix des produits : **de $1.99 à $499.99**.
- **Ajout de Colonnes Calculées** :
  - `Début du mois` et `Début de la semaine` dans la table **Calendar**.

---

### 2. Modélisation Relationnelle 🗄️
- **Modèle en Étoile** :
  - Relation 1:N entre la table de faits **Sales** et les tables dimensionnelles (**Products**, **Stores**, **Calendar**).
- **Optimisations** :
  - Création d’une hiérarchie temporelle : `Début du mois > Début de la semaine > Date`.
  - Masquage des clés étrangères dans la table **Sales** pour simplifier la vue rapport.

---

### 3. Calculs & Mesures DAX 🧮
- **Colonnes Calculées** :
  - `Coût` et `Prix` tirés de la table **Products**.
  - `Revenu` : `Prix x Quantité`.
  - `Profit` : `Revenu - Coût`.
- **Mesures Clés** :
  - **Nombre total de commandes** : `Total Orders`.
  - **Revenu total** : `Total Revenue`.
  - **Profit total** : `Total Profit`.
- **Mesures Avancées (Bonus)** :
  - Calculs de `Revenu Total` et `Profit Total` sans utiliser les colonnes calculées.

---

### 4. Création du Rapport 📊
- **Visualisations Clés** :
  - **Cartes KPI** : Nombre total de commandes, revenu total, et profit total pour le mois en cours.
  - **Barres** : Nombre total de commandes par catégorie de produit.
  - **Courbe** : Revenu total avec hiérarchie temporelle (axe X).
- **Interactions et Formatage** :
  - **Slicer** : Filtre par localisation des magasins.
  - Alignement logique des visuels pour une navigation intuitive.

---

## 📈 Insights Clés

- **Performance des Ventes** :
  - Le revenu total pour le mois en cours s'élève à **X $** (remplacer par votre résultat final).
- **Produits les Plus Performants** :
  - La catégorie **Y** génère le plus grand nombre de commandes.
- **Tendances** :
  - Les ventes suivent une saisonnalité marquée, avec des pics lors des fêtes.

---

## 🛠️ Étapes Techniques Principales
- **Power Query** :
  - Profilage des données et ajout de colonnes calculées.
- **Modélisation Relationnelle** :
  - Conception d’un modèle en étoile.
- **Formules DAX** :
  - Création de mesures pour les KPI financiers et opérationnels.
- **Visualisations Interactives** :
  - Graphiques, slicers et mise en page ergonomique.

---

## 📄 Fichier Power BI Principal
- **Nom** : `Toy_Store_KPI_Report.pbix`
- **Description** : Tableau de bord interactif pour suivre les KPI de ventes et explorer les tendances par produit et localisation.
- **Lien** : [Télécharger le fichier Power BI](#) <!-- Ajouter un lien Google Drive ici -->

---

## 🏆 Livrables
1. **Tableau de Bord Interactif** : "Toy Store KPI Report".
2. **Rapport Publié** : Hébergé sur Power BI Service.
3. **Documentation** : Insights clés et mesures DAX.

---

## 📚 Ressources
- [Documentation Power BI](https://learn.microsoft.com/fr-fr/power-bi/)
- [Guide DAX](https://dax.guide/)
