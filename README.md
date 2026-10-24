# 🛡️ Cyber Africa Forum — Analyse des tendances LinkedIn (Python + Power BI)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat&logo=selenium&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Statut](https://img.shields.io/badge/statut-terminé-success?style=flat)

> Outil de veille qui collecte automatiquement des publications LinkedIn, les nettoie avec Python et les restitue dans un tableau de bord Power BI pour identifier les tendances autour de la **cybersécurité et de l'IA en Afrique**.
> Réalisé pour le **Cyber Africa Forum (CAF)**.

---

## 🎯 Contexte et objectifs

Le Cyber Africa Forum avait pour thème :
**« Risques cybernétiques et Intelligence Artificielle : quelles stratégies de défense face aux nouvelles menaces numériques ? »**

L'objectif : développer un outil capable d'identifier les tendances et les sujets qui font réagir sur LinkedIn autour de ce thème, pour nourrir la préparation et la communication du forum.

## 🧭 Démarche (pipeline de bout en bout)

```
Mots-clés  ──▶  Scraping Python  ──▶  Nettoyage  ──▶  CSV propre  ──▶  Dashboard Power BI
```

### 1. Définition des mots-clés
Ciblage des publications liées au thème du forum :
`Protection des données Afrique` · `Cyberattaques Afrique` · `Cybersécurité et IA en Afrique` · `Sécurité informatique Afrique` · `Intelligence artificielle Afrique` · `Cyber menaces Afrique` · `Sécurité des systèmes Afrique` · `Conférence IA Afrique`

### 2. Web scraping (Python / Selenium)
- Connexion automatisée à LinkedIn avec **Selenium** (WebDriver)
- Extraction des publications : **auteur, date, titre, nombre de likes, commentaires, republications**
- Export des résultats en CSV

### 3. Nettoyage et préparation des données
- Suppression des symboles et caractères non pertinents
- Traitement et normalisation des dates (**Pandas**, **dateparser**)
- Production d'un jeu de données propre : `Pub_linkedin_datacleaned.csv`

### 4. Tableau de bord Power BI
- Volume de publications par mot-clé et dans le temps
- Engagement (likes, commentaires, republications)
- Auteurs et sujets les plus influents

## 📚 Livrable complémentaire : étude comparative de Data Modeling

En parallèle, une étude comparant **5 techniques de modélisation de données** pour choisir la plus adaptée au reporting :

| Technique | Point fort | Usage typique |
|---|---|---|
| Star Schema | Simple, lisible, requêtes rapides | Tableaux de bord (Power BI, Excel) |
| Snowflake | Moins de redondance | Reporting hiérarchique |
| Data Vault 2.0 | Flexible et évolutif | Entrepôts de données modernes, audit |
| Galaxy Schema | Plusieurs faits partagent des dimensions | Analyses multi-processus |
| Anchor Modeling | Ultra-normalisé, historisation | Environnements très dynamiques |

➡️ Le **Star Schema** a été retenu pour le dashboard : lisibilité et performance dans Power BI.

## 🖼️ Aperçu du tableau de bord

![Dashboard – page 1](Capture%20d_%C3%A9cran%20%26%20Pr%C3%A9sentation_/Page1.jpg)

| Page 2 | Page 3 |
|---|---|
| ![](Capture%20d_%C3%A9cran%20%26%20Pr%C3%A9sentation_/Page_2.jpg) | ![](Capture%20d_%C3%A9cran%20%26%20Pr%C3%A9sentation_/Page__3.jpg) |

## 📁 Contenu du dépôt

| Élément | Description |
|---|---|
| [`Scaping_PUB_Linkedin.ipynb`](Scaping_PUB_Linkedin.ipynb) | Notebook Python : scraping (Selenium) et nettoyage (Pandas) |
| [`Données/`](Donn%C3%A9es) | Données brutes, intermédiaires et nettoyées ([`Pub_linkedin_datacleaned.csv`](Donn%C3%A9es/Pub_linkedin_datacleaned.csv)) |
| [`Dashboard Power BI (.pbix)`](Dashboard%20POWER%20BI_Analyse_des_Tendances_Linkedin.pbix) | Tableau de bord Power BI |
| [Dashboard (PDF)](Capture%20d_%C3%A9cran%20%26%20Pr%C3%A9sentation_/DASHBOARD_Analyse%20des%20Tendances_Linkedin%20pdf.pdf) | Export PDF du tableau de bord |
| [Présentation (PDF)](Capture%20d_%C3%A9cran%20%26%20Pr%C3%A9sentation_/PRESENTATION%20POWER%20POINT%20DU%20PROJET_TENDANCES%20LINKEDIN_CAF2024_.pdf) | Présentation du projet |
| [Documentation technique](Documentation%20Technique.pdf) | Documentation complète de l'outil |
| [Étude de Data Modeling](%C3%89tude%20comparative%20des%20techniques%20de%20Data%20Modeling.pdf) | Comparatif de 5 techniques de modélisation |

## ▶️ Utilisation

1. Ouvrir le notebook `Scaping_PUB_Linkedin.ipynb` dans Jupyter ou Google Colab.
2. Renseigner ses propres identifiants LinkedIn **localement** (ne jamais les publier dans le dépôt).
3. Lancer les cellules pour collecter puis nettoyer les publications.
4. Ouvrir le fichier `.pbix` dans **Power BI Desktop** et actualiser la source de données.

> ⚠️ Le scraping doit respecter les conditions d'utilisation de LinkedIn. Ce projet a été réalisé à des fins d'analyse et de veille.

## 👤 Auteur

**Ismaël Traoré** — Développeur Data & IA
📧 contact.traoreimael@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/ismael-traor%C3%A9-m-4007a2225/)
