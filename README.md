# ToxiBERT : Classification de Commentaires Toxiques avec BERT

Ce dépôt contient un projet de **classification de commentaires toxiques** utilisant le modèle **BERT (Bidirectional Encoder Representations from Transformers)**. Ce projet utilise des techniques de traitement automatique du langage naturel (NLP) pour classer les commentaires comme toxiques ou non-toxiques, avec pour objectif de soutenir les efforts de modération de contenu.

## Présentation du Projet

L'objectif de ce projet est de construire un **modèle de classification de texte** capable d'identifier la toxicité des commentaires à partir d'un ensemble de données annotées. En utilisant le modèle **BERT**, le projet ajuste un transformeur pré-entraîné pour prédire avec précision si un commentaire est toxique ou non.

### Principales Fonctionnalités :
- **Classification des Commentaires Toxiques** : Le modèle identifie si un commentaire est toxique ou non-toxique.
- **Prédiction Interactive** : Une fonction permet la prédiction en temps réel de la toxicité des commentaires soumis par les utilisateurs.
- **Visualisation des Données** : Analyse et visualisation de la répartition des commentaires toxiques à l’aide de graphiques.

## Jeu de Données

Le jeu de données utilisé dans ce projet contient des commentaires annotés comme toxiques ou non-toxiques. Il est divisé en **ensemble d'entraînement**, **ensemble de validation** et **ensemble de test** pour garantir une évaluation fiable des performances du modèle.

## Technologies Utilisées

Les bibliothèques et outils suivants ont été utilisés pour développer, entraîner et évaluer le modèle :

- **Pandas** : Pour la manipulation et le nettoyage des données, comme la lecture des fichiers CSV et le traitement des textes.
- **Scikit-learn** : Utilisé pour diviser les données en ensembles d'entraînement, de test et de validation.
- **PyTorch** : La bibliothèque principale utilisée pour construire et entraîner le modèle BERT.
- **Transformers** : Bibliothèque de Hugging Face fournissant des modèles pré-entraînés comme BERT et des outils pour le fine-tuning.
- **Matplotlib** et **Seaborn** : Bibliothèques de visualisation utilisées pour analyser la répartition des commentaires toxiques.
- **Expressions Régulières (re)** : Utilisées pour le nettoyage des données textuelles, comme la suppression des caractères spéciaux.
- **NumPy** : Pour les opérations numériques et la gestion des grands tableaux de données.

## Architecture du Modèle

Le modèle **BERT** a été ajusté (fine-tuned) sur le jeu de données de classification des commentaires toxiques. Le processus d'ajustement consiste à modifier les poids du modèle pré-entraîné pour répondre à la tâche spécifique de classification des commentaires.

### Étapes Clés :
1. **Prétraitement** : Les données textuelles sont nettoyées à l’aide d'expressions régulières et tokenisées avec le tokenizer de BERT.
2. **Entraînement du Modèle** : Le modèle est ajusté sur les données d'entraînement à l'aide de PyTorch et de la bibliothèque Transformers.
3. **Évaluation** : Les performances du modèle sont évaluées avec des métriques de classification telles que **précision**, **rappel** et **F1-score**.

## Métriques d'Évaluation

Les performances du modèle sont évaluées à l'aide des métriques suivantes :

- **Précision** : 0.9724
- **Précision pondérée** : 0.7529
- **Rappel** : 0.6194

## Comment Utiliser

1. Cloner le dépôt :
   ```
   git clone https://github.com/utilisateur/classification-commentaires-toxiques-bert.git
   cd classification-commentaires-toxiques-bert
   ```

2. Installer les dépendances requises :
   ```
   pip install -r requirements.txt
   ```

3. Exécuter le script d'entraînement :
   ```
   python train.py
   ```

4. Pour prédire la toxicité d’un nouveau commentaire, utiliser la fonction `predict_user_input()` dans le fichier `predict.py` :
   ```python
   from predict import predict_user_input

   commentaire = "Votre commentaire ici"
   prediction = predict_user_input(commentaire)
   print(f"Prédiction : {prediction}")
   ```

## Résultats

Le modèle BERT ajusté atteint une haute précision et peut prédire efficacement si un commentaire est toxique. Cette solution peut être mise en œuvre dans les systèmes de **modération de contenu** pour automatiser la détection de commentaires nuisibles sur les plateformes.

## Améliorations Futures

- **Optimisation des Hyperparamètres** : Explorer différentes configurations d’hyperparamètres pour améliorer la précision et le rappel.
- **Inclusion de Données Supplémentaires** : Incorporer des jeux de données plus diversifiés pour améliorer la généralisation du modèle.
- **Déploiement** : Déployer le modèle en tant que service web pour la classification des commentaires en temps réel.

## Contribution

N'hésitez pas à soumettre une pull request ou à ouvrir une issue si vous souhaitez contribuer à ce projet.
