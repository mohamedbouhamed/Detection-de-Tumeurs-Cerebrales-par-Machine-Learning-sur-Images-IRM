# Détection de Tumeurs Cérébrales par Machine Learning sur Images IRM

## Description

Ce projet implémente un modèle de classification d’images IRM cérébrales pour détecter la présence de tumeurs.  
Le modèle est basé sur une architecture de deep learning pré-entraînée VGG16, adaptée à notre problème de classification binaire (tumeur vs pas tumeur).

## Base de données

- **Nom** : Brain MRI Images for Brain Tumor Detection  
- **Source** : [Kaggle - navoneel/brain-mri-images-for-brain-tumor-detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)  
- **Description** :  
  - Contient des images IRM cérébrales annotées en deux classes : présence ou absence de tumeur.  
  - Images en formats JPG, divisées en dossiers `yes` (avec tumeur) et `no` (sans tumeur).

## Fonctionnalités principales

- Prétraitement des images : redimensionnement à 224×224 pixels pour correspondre à l’entrée du modèle VGG16.  
- Utilisation de VGG16 pré-entraîné sur ImageNet (sans les couches fully connected finales).  
- Ajout de nouvelles couches denses pour la classification binaire.  
- Entraînement avec transfert learning (couches VGG16 gelées).  
- Évaluation de la performance avec métriques d’accuracy et loss.
