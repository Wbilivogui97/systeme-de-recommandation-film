# **Système de Recommandation de Films**

## **Auteurs**  
Ce projet a été réalisé par WOYE BALLA BILIVOGUI,KERFALLA SYLLA et MOHAMED MARIE CAMARA dans le cadre du cours de **Data Mining**.

## **Contexte du Projet**  
L’objectif principal de ce projet était de concevoir un système capable de recommander des films aux utilisateurs en fonction de leurs préférences ou d’autres critères, tels que :  
- **Le genre** du film (Action, Comédie, Drame, etc.).  
- **Le réalisateur** ou les vedettes principales.  
- **L'année de sortie** ou la popularité.  

Nous avons utilisé différentes techniques apprises en cours de data mining pour développer une solution robuste, en appliquant des concepts de filtrage collaboratif et de similarité.

## **Colonnes du Jeu de Données**  
Le jeu de données utilisé contient les informations suivantes :  

| **Colonne**          | **Description**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|
| `name`               | Nom ou titre du film.                                                          |
| `rating`             | Classification par âge (ex. : PG, R).                                          |
| `genre`              | Catégorie ou type du film (Action, Comédie, etc.).                             |
| `year`               | Année de sortie du film.                                                       |
| `released`           | Date exacte de sortie (ex. : 13 June 1980).                                    |
| `score`              | Note moyenne attribuée par les spectateurs.                                    |
| `votes`              | Nombre total de votes enregistrés.                                             |
| `director`           | Nom du réalisateur.                                                           |
| `writer`             | Nom du scénariste.                                                            |
| `star`               | Acteur principal ou vedette.                                                  |
| `country`            | Pays d'origine du film.                                                       |
| `budget`             | Budget de production (en USD).                                                |
| `gross`              | Recettes totales générées (en USD).                                            |
| `company`            | Société de production.                                                        |
| `runtime`            | Durée totale du film (en minutes).                                             |

## **Approches Utilisées**
### **1. Filtrage Colaboratif**
Nous avons utilisé les attributs des films, comme le genre, le réalisateur ou les vedettes principales, pour identifier des films similaires. Ces informations ont été combinées dans une seule colonne (`cat_feature`) pour faciliter la vectorisation.

### **2. Techniques de Similarité**
La similarité entre les films a été calculée en utilisant :    
- **Similarité Cosinus** : Pour mesurer la proximité entre les films en fonction des vecteurs générés.
## **Étapes Principales**
1. **Tout le processus de data mining** :
   - Nettoyage des colonnes et traitement des valeurs manquantes.
   - Création d'une nouvelle colonne combinant les informations pertinentes (`cat_feature`).
   - Etc...
2. **Vectorisation des Données** :
   - Utilisation de `CountVectorizer` pour transformer les données textuelles en vecteurs numériques exploitables.

3. **Calcul de la Similarité** :
   - Application de la similarité cosinus pour comparer les films.

4. **Recommandations** :
   - Création d'une fonction permettant de suggérer des films similaires à un titre donné.

## **Technologies Utilisées**
- **Python3.11** : Langage principal pour le traitement des données et la construction du modèle.
- **Bibliothèques** :
  - `pandas` : Manipulation et nettoyage des données.
  - `numpy` : Calculs numériques avancés.
  - `scikit-learn` : Vectorisation Countvectorizer et calcul de similarité.
  - `matplotlib` et `seaborn` : Visualisation des données.

## **Exemple d'Utilisation**
Pour obtenir des recommandations de films :  
```python
# Exemple de recommandation
recommend_movies("The Shining")
Le système renverra une liste de films similaires en fonction des caractéristiques de "The Shining".
## **Résultats Attendus**
- **Recommandations pertinentes** :
En fonction du genre, du réalisateur et d'autres caractéristiques.  
- **Flexibilité** :
 Possibilité de personnaliser les critères de similarité.  
## Contribution
Ce projet a été réalisé en équipe pour encourager la collaboration et l'application des concepts théoriques de **Data Mining** à un cas pratique.
