# TP_MNIST_GENERATIVE — Modèles génératifs avec PyTorch

## Présentation du projet

Ce projet a pour objectif de découvrir et d'explorer les modèles de Deep Learning avec **PyTorch**, en utilisant le dataset **MNIST** (Modified National Institute of Standards and Technology).

Il consiste à créer, entraîner, tester et explorer trois types de modèles :

- Un modèle discriminatif basé sur un réseau de neurones convolutif (CNN).
- Un auto-encodeur simple (Autoencoder).
- Un auto-encodeur variationnel (Variational Autoencoder — VAE).

L'objectif est de comprendre les différences entre les modèles de classification et les modèles génératifs, ainsi que leur fonctionnement sur des images de chiffres manuscrits.

## Objectifs pédagogiques

- Configurer un environnement Python avec UV.
- Manipuler des tenseurs avec PyTorch.
- Charger et explorer le dataset MNIST.
- Construire et entraîner un modèle discriminatif.
- Évaluer les performances d'un modèle de classification.
- Comprendre le fonctionnement d'un auto-encodeur.
- Explorer les représentations latentes.
- Comprendre le fonctionnement d'un VAE.
- Générer de nouvelles images à partir d'un espace latent.

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python 3.11 | Langage de programmation |
| UV | Gestion de l'environnement et des dépendances |
| PyTorch | Construction et entraînement des modèles |
| Torchvision | Chargement et transformation de MNIST |
| NumPy | Manipulation des données numériques |
| Matplotlib | Visualisation des images et des résultats |
| TorchEval | Outils d'évaluation des modèles |
| Jupyter Notebook | Développement et expérimentation |

## Dataset : MNIST

Le dataset MNIST contient 70 000 images de chiffres manuscrits allant de 0 à 9.

Il est réparti en deux ensembles :

- **Entraînement :** 60 000 images.
- **Test :** 10 000 images.

Caractéristiques des images :
- Dimensions : 28 × 28 pixels.
- Couleur : niveaux de gris.
- Nombre de classes : 10.
- Valeurs des pixels : normalisées entre 0 et 1.

Le dataset est téléchargé automatiquement grâce à `torchvision.datasets.MNIST`.

## Installation et configuration

### 1. Cloner le projet

```bash
git clone <URL_DU_DEPOT>
cd TP_MNIST_GENERATIVE
```

### 2. Créer l'environnement Python

```bash
uv python install 3.11
uv venv --python 3.11
```

### 3. Activer l'environnement

Sur macOS / Linux :

```bash
source .venv/bin/activate
```

Sur Windows :

```powershell
.venv\Scripts\Activate.ps1
```

### 4. Installer les dépendances

```bash
uv add ipykernel
uv add torch
uv add torchvision
uv add torcheval
uv add matplotlib
uv add numpy
uv add tqdm
```

### 5. Enregistrer le Kernel Jupyter

```bash
python -m ipykernel install --user --name tp-mnist-generative --display-name "Python 3.11 (TP_MNIST_GENERATIVE)"
```

### 6. Lancer le projet

Ouvrir le dossier dans VS Code, puis ouvrir le notebook :

`TP_MNIST_PyTorch.ipynb`

Sélectionner le kernel Python 3.11 de l'environnement `.venv` et exécuter les cellules.

## Travail réalisé

### Partie 1 — Modèle discriminatif (CNN)

Construction d'un réseau de neurones convolutif permettant de classifier les images MNIST.

Étapes :
- Construction de l'architecture CNN.
- Entraînement sur les données MNIST.
- Évaluation sur les données de test.
- Calcul de la précision (Accuracy).
- Visualisation des prédictions et des courbes d'apprentissage.

### Partie 2 — Auto-encodeur simple (AE)

Construction d'un modèle permettant d'apprendre une représentation compressée des images et de les reconstruire.

Étapes :
- Construction de l'encodeur.
- Construction du décodeur.
- Apprentissage des représentations latentes.
- Reconstruction des images.
- Comparaison entre les images originales et reconstruites.

### Partie 3 — Auto-encodeur variationnel (VAE)

Construction d'un modèle génératif permettant d'apprendre une distribution probabiliste dans un espace latent.

Étapes :
- Encodage des images en moyenne et variance.
- Application de la technique de reparamétrisation.
- Calcul de la perte de reconstruction.
- Calcul de la divergence KL.
- Entraînement du modèle.
- Génération de nouvelles images à partir de vecteurs latents aléatoires.

## Résultats attendus

À la fin du projet, les expérimentations permettent de :

- Reconnaître les chiffres manuscrits avec un CNN.
- Reconstruire des images avec un auto-encodeur.
- Explorer les représentations latentes.
- Générer de nouvelles images de chiffres manuscrits avec un VAE.
- Comparer les approches discriminatives et génératives.
# TP_MNIST_GENERATIVE
