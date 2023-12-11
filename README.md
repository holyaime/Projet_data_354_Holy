# Projet_data_354_Holy
Ce projet vise à développer un modèle d'apprentissage automatique pour la classification d'images en utilisant PyTorch.Le code est conçu pour fonctionner avec des données spécifiques contenues sur ce site https://zindi.africa/competitions/microsoft-rice-disease-classification-challenge.


##Objectif
L'objectif principal est de classer les images en trois catégories : 'healthy', 'blast', et 'brown'. Le modèle est basé sur l'architecture ResNet18 pré-entraînée.

## Structure du Projet
Importations de Bibliothèques: Les bibliothèques nécessaires au projet sont importées, y compris PyTorch, pandas, et matplotlib.

Chargement des Données: Les données d'entraînement, de test et de soumission sont chargées à partir de fichiers CSV, et un aperçu des données est fourni.

Prétraitement des Images: Les images sont chargées, certaines sont supprimées, il s'agit de tous images infrarouge et les données sont divisées en ensembles d'entraînement et de validation. Un diagramme à barres illustre la répartition des étiquettes.

Création des Dossiers d'Images: Les images sont copiées dans des dossiers appropriés(l'espace de travail) pour faciliter le chargement des données.

Définition du Dataset et des Transformations: Un dataset personnalisé est créé pour gérer les données d'entraînement, de validation et de test. Des transformations d'images sont définies, notamment le redimensionnement et la normalisation.

Création des Chargeurs de Données: Des DataLoader sont créés pour charger les données pendant l'entraînement et l'évaluation du modèle.

Création du Modèle: Une classe de modèle personnalisé est créée en utilisant ResNet18, avec une couche de sortie adaptée au nombre de classes.

Entraînement du Modèle: Le modèle est entraîné avec différentes configurations d'optimiseurs. Les pertes d'entraînement et de validation sont suivies.

## Utilisation
Assurez-vous que toutes les bibliothèques requises sont installées (torch, pandas, etc.). vous les verrai toutes dans la partie code.
Placez les données dans les répertoires spécifiés.
Exécutez le code pour entraîner le modèle et générer des prédictions.



## Remarques
Le modèle utilise la GPU s'il est disponible, sinon il utilise le CPU.
Les performances du modèle peuvent être améliorées en ajustant encore les hyperparamètres et en faisant une validation croisée.

## Analyse Graphique après la Phase d'Entraînement

Le graphique suivant illustre l'évolution de la perte d'entraînement, de la perte de validation et de la précision de validation au fil des époques.

Ce graphique présente deux sous-graphiques :

Courbe de Perte d'Entraînement: Montre la variation de la perte d'entraînement et de validation au fil des époques.
Courbe de Précision de Validation: Illustration de la précision du modèle sur l'ensemble de validation au fil des époques.
Ces graphiques sont essentiels pour évaluer la performance du modèle pendant l'entraînement et ajuster les hyperparamètres si nécessaire.

# Test du Modèle

Après l'entraînement, le modèle est testé sur un ensemble de données distinct. Les prédictions sont générées à l'aide du modèle entraîné avec les meilleurs poids obtenus pendant l'entraînement.
Ce bloc de code charge le modèle entraîné, effectue des prédictions sur les données de test et stocke les résultats dans la liste predictions.

