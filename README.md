# Classification_MobileNetV2_COVID-19

Ce projet utilise le modèle MobileNetV2 pour effectuer la classification d’images, avec un cas d’application axé sur la détection de COVID-19 à partir d’images CT-SCAN (https://www.kaggle.com/datasets/plameneduardo/sarscov2-ctscan-dataset). Le pipeline inclut la préparation des données, le prétraitement des images, l'entraînement et l'évaluation du modèle.

## Objectifs
- Classifier les images CT-SCAN en différentes catégories (non COVID-19 et COVID-19).
- Exploiter un modèle pré-entraîné (MobileNetV2) un modèle de réseau de neurones convolutifs (CNN) pour bénéficier du transfert d’apprentissage et améliorer les performances.

---

## Configuration et prétraitement des données

1. **Chargement des données**  

3. **Prétraitement des images**
   Les images ont été redimensionnées à 224x224 pixels, conformément aux exigences du modèle MobileNetV2, et converties au format RGB. 
  
2. **Division des données**
   Les données ont été divisées en trois ensembles :
   - **Entraînement** : Pour entraîner le modèle.
   - **Validation** : Pour ajuster les hyperparamètres et éviter le surapprentissage.
   - **Test** : Pour évaluer les performances finales du modèle.

---

## Modélisation avec MobileNetV2

1. **MobileNetV2**
   - Utilisation du modèle pré-entraîné MobileNetV2 pour tirer parti des poids optimisés sur le dataset ImageNet.
   - Les couches supérieures ont été ajustées pour s’adapter au nombre de classes de ce projet.

2. **Compilateur**
   - Optimiseur : Adam.
   - Fonction de perte : Entropie croissée (catégorielle).
   - Métrique : `accuracy` pour évaluer les performances.

3. **Entraînement**
   - Nombre d’époques : 100
   - Utilisation des ensembles d’entraînement et de validation.

---

## Résultats et évaluation

- Les performances du modèle sont évaluées sur l’ensemble de test.
- Les métriques incluent : 
  - Précision (évaluation des bonnes prédictions)
  - F1 score, recall...
  - Matrice de confusion

---
