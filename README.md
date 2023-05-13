# Datasets_Analysis

Week 3 Day 5 - Project: Analysing various datasets and understanding business teams.  
NB: This project was done in French.

Pour chaque lot de données, nous voulons comprendre l'essentiel et être capable d'évaluer la pertinence des données:  
- **Description** 
  - les donnéees principales
  - le type (données brutes ou agrégées)
  - les indicateurs  
- **Sens global**
  - Qui doit être responsable de mettre à jour ce jeu de données en termes métier ? 
  - Pourquoi est-il intéressant ? 
  - Quelles tendances métiers reflète-t-il ?  
- **Limites**
  - Quelles données seraient-elles intéressantes d'avoir en complément ? 
  - Y-a-t-il des données incomplètes ? 
  - Quelles questions serait-il intéressant de poser aux personnes métiers pour mieux comprendre le sens global ?

## Énergie

6 jeux de données de [Enedis](https://data.enedis.fr/pages/accueil/).  

Production électrique annuelle totale par filière, par maille géographique :
- [Région](https://data.enedis.fr/explore/dataset/production-electrique-par-filiere-a-la-maille-region/)
- [Département](https://data.enedis.fr/explore/dataset/production-electrique-par-filiere-a-la-maille-departement/)
- [Commune](https://data.enedis.fr/explore/dataset/production-electrique-par-filiere-a-la-maille-commune/)
- [EPCI](https://data.enedis.fr/explore/dataset/production-electrique-par-filiere-a-la-maille-epci/) (Établissements Publics de Coopération Intercommunales)
- [IRIS](https://data.enedis.fr/explore/dataset/production-electrique-par-filiere-a-la-maille-iris/) (Ilots Regroupés pour l'Information Statistique)   

Consommation journalière par catégorie de client :  
- [Bilan électrique](https://data.enedis.fr/explore/dataset/bilan-electrique-transpose/)

**Description**  

Les 5 premiers jeux de données restituent la production électrique annuelle totale et le nombre de sites, par filière et par domaine de tension et de puissance à la maille géographique en question (région, département, commune, EPCI ou IRIS) sur le réseau géré par Enedis. Les indicateurs sont le nombres de sites et l'énergie annuelle produite  par type de site (photovoltaïque, éolien, hydraulique, cogénération, bioénergies, autres filières). Le 6ème jeu de données est plus simple et montre la consommation journalière par catégorie de client, l'indicateur est ici la puissance moyenne journalière. Les données sont agrégées, c'est à dire qu'elles ont été nettoyées, préparées et calculées. De plus, les informations personnelles et secretes ont été protégées.

**Sens global**  

Enedis est responsable de [la collecte, la gestion et la mise à jour des données](https://www.enedis.fr/gerer-les-donnees). Les données sont disponibles sous différents formats (en CSV, JSON, Excel), les fichiers géographiques et l'utilisation via API. Leur site met également à disposition des outils de visualisation rapide (tableaux, cartes et graphiques) très utiles (voir graphe ci-dessous).  

<img src=/Graph_Enedis.jpg />

**Limites**  

Il manque clairement des sources d'énergies importantes telles que le nucléaire et les énergies fossiles (charbon, gaz, fioul). Le jeu de données semble focalisé sur les énergies renouvelables alors que ceci n'est pas clairement explicité. Le détail de la source "autres filières" n'est pas clair également. Il serait utile de poser ces questions aux membres des équipes métiers ou gestionnaires des données.

## Ville de Paris

3 jeux de données de l'[Apur](https://opendata.apur.org/) (Atelier Parisien d'Urbanisme) :
- [Quartiers de Paris](https://opendata.apur.org/maps/quartier-de-paris)
- [Voies](https://opendata.apur.org/maps/voie)
- [Équipements ponctuels liés aux cultes](https://opendata.apur.org/maps/equipement-ponctuel-culte)

**Définition**  

Le 1er jeu présente les 80 quartiers administratifs de Paris, le deuxième toutes les voies publiques et privées (rues, avenues, etc.), et le troisième jeu les équipements ponctuels liés aux cultes (lieu de culte, orphelinat confessionnel, couvent, congrégation religieuse et séminaire). Les indicateurs les plus importants sont les coordonnées géospatiales, ainsi que les imformations supplémentaires suivant les jeux (taille des quartiers, longueur des voies, 


**Sens global**  

Les données sont disponibles au format CSV simple, ainsi que les formats de fichiers géospatiaux KML, Shapefile et GeoJSON. L'Apur construit, enrichit et capitalise de nombreuses [données géographiques](https://www.apur.org/fr/geo-data) sur Paris et la Métropole du Grand Paris. La démarche Open Data initiée par l’Apur vise à libérer régulièrement de nouvelles données issues des études de l’Atelier et participe ainsi à l’innovation métropolitaine et au partage des ressources publiques. Le site offre la visualisation des données sur une carte interactive sur laquelle on peut utiliser des filtres (correspondant aux colonnes de la table de données). Sur l'image ci-dessous on voit les quartiers de Paris filtrés par longueur, en ne gardant que les plus petits (moins de 1 861 unités inconnues).

<img src=/Carte_Paris_Apur.jpg />

**Limites**  

Le jeu de données des équipements ponctuels liés aux cultes par exemple, ne permet pas de filtrer par type de lieux, cette information fait partie du nom entier, il aurait pu être utile de créer une colonne pour les sous-catégories afin de pouvoir les filtrer.

## Assurance Maladie

Une base de données de [Ameli (Assurance Maladie)](https://assurance-maladie.ameli.fr/etudes-et-donnees/donnees/liste-bases-de-donnees-open-data) :  
- Base complète [Open Damir](https://assurance-maladie.ameli.fr/etudes-et-donnees/open-damir-depenses-sante-interregimes) sur les dépenses de l'ensemble des régimes d'assurance 

**Définition**  

Open Damir est une base complète sur les dépenses d'assurance maladie, contenant les données de l'ensemble des régimes d'assurance maladie en France entière depuis janvier 2009, données mensuelles mises à jour chaque année. D'après les descriptions des données, les dépenses sont détaillées six axes d'analyse (période, prestation, organisme de prise en charge, bénéficiaire des soins, professionnel de santé exécutant, professionnel de santé prescripteur), quatre indicateurs de montant (total de la dépense, base de remboursement de l’Assurance Maladie, montant remboursé, dépassements d’honoraires des professionnels de santé) et trois indicateurs de volume (dénombrement, quantité, coefficient). Il semble que les données soient brutes.

**Sens global**  

Toutes les données sont extraites du système national des données de santé (SNDS). Le [SNDS](https://www.snds.gouv.fr/SNDS/Accueil) est géré par la Caisse Nationale de l’Assurance Maladie des Travailleurs Salariés (CNAMTS). Il est difficile d'en évaluer l'intérêt car la base de données comporte beaucoup d'indicateurs et d'axes d'analyse, mais c'est ce qui en fait aussi une base intéressante car beaucoup de possibilités d'analyses existent.

**Limites**  

Les fichiers de la base de données (un fichier CSV pour chaque mois) sont très volumineux et difficiles à télécharger, probablement encore plus à lire. Il serait peut être judicieux de créer une base beaucoup moins lourde destinée au public ou à la visualisation en direct en ne gardant que les informations strictement nécessaires. Mais je vois que la plateforme propose aussi des [synthèses des dépenses mensuelles](https://assurance-maladie.ameli.fr/etudes-et-donnees/par-theme/depenses-assurance-maladie/synthese-depenses-mensuelles) sous formes de tableaux statistiques (données agrégées).  

## Sources de données ouvertes (Open Data)

Beaucoup de sites existent pour trouver des ensembles de données :
- [Kaggle](https://www.kaggle.com/datasets)
- [Google Dataset Search](https://datasetsearch.research.google.com/)
- [DataHub.io](https://datahub.io/collections)
- [France - Data.gouv.fr](https://www.data.gouv.fr/fr/datasets/)
- [US - Data.gov](https://data.gov/)
- [FiveThirtyEight](https://data.fivethirtyeight.com/)
- [Our World in Data](https://ourworldindata.org/)
- [The Pudding Data](https://github.com/the-pudding/data)
- [ICIJ Data Journalism](https://www.icij.org/tags/data-journalism/)
- [UCI Machine Learning](https://archive.ics.uci.edu/ml/datasets.php)
- [Earth Data NASA](https://www.earthdata.nasa.gov/)
- [CERN Open Data](http://opendata.cern.ch/)
- [Global Health Observatory (WHO)](https://apps.who.int/gho/data/node.home)
- [British Film Institute](https://www.bfi.org.uk/industry-data-insights)
- [FBI Crime Data Explorer](https://cde.ucr.cjis.gov/)
- [Academic Torrents](https://academictorrents.com/checkb.htm)
- [GitHub - Awesome Public Datasets](https://github.com/awesomedata/awesome-public-datasets)
