# Datasets_Analysis

Week 3 Day 5 - Project: Understanding business teams by analysing their set of data.  
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

3 jeux de données de l'[Apur](https://opendata.apur.org/) :
- [Quartiers de Paris](https://opendata.apur.org/maps/quartier-de-paris)
- [Voies](https://opendata.apur.org/maps/voie)
- [Lieux de culte](https://opendata.apur.org/maps/equipement-ponctuel-culte)

## Assurance Maladie

Une base de données de [Ameli (Assurance Maladie)](https://assurance-maladie.ameli.fr/etudes-et-donnees/donnees/liste-bases-de-donnees-open-data) :  
- [Open Damir](https://assurance-maladie.ameli.fr/etudes-et-donnees/open-damir-depenses-sante-interregimes) - base complète sur les dépenses d'assurance maladie (données de l'ensemble des régimes d'assurance maladie en France entière depuis janvier 2009, données mensuelles mises à jour chaque année).
