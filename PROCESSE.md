# Processus de préparation des templates email

## 1. Normalisation des images

- Convertir toutes les images au même format
- **Optimiser l'espace** dans toutes les images pour respecter le layout du design
- **Nommer les images** avec des colonnes et numéros (ex: `col1_img1.jpg`)

## 2. Structure HTML/CSS

- Le HTML et le CSS doivent être dans **un seul fichier**
- **Importer les polices** en haut du fichier et les appliquer dans les styles des éléments
  - Exemple pour Poppins : `@import url('https://fonts.cdnfonts.com/css/poppins');`
- **Créer un tableau** avec colonnes gauche/droite
- **Ajuster la largeur** avec hauteur automatique pour maintenir le design dans Gmail

## 3. Hébergement des images

- Changer les URLs des images vers l'URL externe du projet Git
- Exemple (branche main) : `https://raw.githubusercontent.com/ihebZm/images_hosting_cfac/main/`

## 4. Tests de responsive

- **Vérifier les modifications** visuelles sur l'application mobile
- **Intentionnellement casser le design** sur les petits et grands écrans
- **Corriger ensuite** en retirant les modifications problématiques

## 5. Configuration de sécurité

- **Rendre le fichier de design problématique** à modifier pour les non-initiés
- **Créer une version compressée ou obfusquée** pour l'aspect sécurité
