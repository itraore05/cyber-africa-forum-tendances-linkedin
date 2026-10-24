# 🛡️ Cyber Africa Forum — Analyse des tendances LinkedIn (Python + Power BI)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Web Scraping](https://img.shields.io/badge/Web%20Scraping-LinkedIn-0A66C2?style=flat)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Statut](https://img.shields.io/badge/statut-terminé-success?style=flat)

> Outil de veille qui collecte automatiquement des publications LinkedIn, les nettoie avec Python et les restitue dans un tableau de bord Power BI pour identifier les tendances autour de la **cybersécurité et de l'IA en Afrique**.
> Réalisé pour le **Cyber Africa Forum (CAF)** — 2025.

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

### 2. Web scraping (Python / Jupyter)
- Connexion automatisée à LinkedIn
- Extraction des publications : **auteur, date, titre, nombre de likes, commentaires, republications**
- Export des résultats en CSV

### 3. Nettoyage et préparation des données
- Suppression des symboles et caractères non pertinents
- Traitement et normalisation des dates
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

## 🖼️ Aperçu

*(captures du dashboard — à compléter)*

## 📁 Contenu du dépôt

| Élément | Description |
|---|---|
| `Scaping_PUB_Linkedin.ipynb` | Notebook Python de scraping et de nettoyage |
| `Données/` | Données brutes et nettoyées (CSV) |
| `Dashboard POWER BI_Analyse_des_Tendances_Linkedin.pbix` | Tableau de bord Power BI |
| `Documentation Technique.pdf` | Documentation complète du projet |
| `Étude comparative des techniques de Data Modeling.pdf` | Étude de modélisation |
| `Capture d_écran & Présentation/` | Captures et présentation |

## ▶️ Utilisation

1. Ouvrir le notebook `Scaping_PUB_Linkedin.ipynb` dans Jupyter ou Google Colab.
2. Renseigner ses propres identifiants LinkedIn **localement** (ne jamais les publier dans le dépôt).
3. Lancer les cellules pour collecter puis nettoyer les publications.
4. Ouvrir le fichier `.pbix` dans **Power BI Desktop** et actualiser la source de données.

> ⚠️ Le scraping doit respecter les conditions d'utilisation de LinkedIn. Ce projet a été réalisé à des fins d'analyse et de veille.

## 👤 Auteur

**Ismaël Traoré** — Développeur Data & IA
📧 contact.traoreimael@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/ismael-traor%C3%A9-m-4007a2225/)
