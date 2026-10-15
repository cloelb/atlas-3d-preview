# ATLAS — Vraie première scène WebGL 3D

**Prototype technique et créatif, pas le jeu final.** Cette version crée et affiche des géométries 3D originales directement dans WebGL2 (maisons, toits, arbres, rivière, chemins, reliefs, avatar et une bibliothèque intérieure). Il ne s'agit pas d'une image fixe ni d'une scène qui mime la profondeur.

## Contenu jouable

- Village 3D avec perspective et caméra suiveuse, rotation au glissement, zoom à la molette ; déplacement par clic/toucher, clavier ZQSD/WASD, joystick tactile.
- Géométrie réellement tridimensionnelle, eau et feuillage animés par shader. Une scène intérieure séparée pour la Maison de la Maire.
- Déclencheurs de lieux et navigation vers la Maison de la Maire, la maison, la bibliothèque et le pavillon.
- Personnage 3D assemblé de volumes simples avec marche articulée, changement fille/garçon, couleurs de peau et de cheveux, tenue. **Le personnage reste un modèle de préproduction**.
- Atlas public de Cloé : Cap et trois Missions, sans inventer de réalisations.
- Missions locales : création de mission, étapes, validation, XP non-dupliqués, Carnet et Cap. Stockage **local au navigateur** uniquement.
- Aucun service externe nécessaire au chargement du moteur : WebGL2 directement, ni npm, ni CDN de moteur. Les polices en ligne sont facultatives.

## Installation GitHub Pages

1. Créer un **nouveau dépôt** `atlas-3d-preview` pour ne pas toucher au dépôt existant `Atlas`.
2. Décompresser l'archive et envoyer les **4 fichiers à la racine** : `index.html`, `styles.css`, `game.js`, `icon.svg`. Ajouter `README.md` si souhaité.
3. Dans `Settings → Pages` : `Deploy from a branch` / `main` / `/(root)` ; enregistrer.
4. Ouvrir `https://cloelb.github.io/atlas-3d-preview/` (après le déploiement).

Un clic direct sur `index.html` fonctionne aussi dans la plupart des navigateurs modernes, car il n'utilise aucun module importé, mais GitHub Pages est conseillé.

## Réalité du niveau de qualité

C'est un **vertical slice WebGL 3D procédural** qui démontre le vrai espace, la caméra, les déplacements et la séparation des scènes ; ce n'est **pas** encore le niveau artistique d'Animal Crossing : les personnages et l'environnement nécessitent des modèles Blender personnalisés, squelettes, textures, éclairages/ombres et animations professionnels.

Un jeu final à cette ambition mérite une architecture de production PlayCanvas/Babylon/Three + assets glTF. Le rendu direct WebGL2 employé ici est volontairement autonome pour éviter les problèmes de chargement déjà rencontrés et démontrer que la 3D fonctionne réellement, avant une éventuelle migration moteur.

## Limitations et sécurité

- Aucune authentification ni synchronisation ; données sauvegardées localement seulement.
- XP de démonstration locale, sans contrôle serveur.
- Les maisons personnelles et la bibliothèque sont des prototypes d'interaction. Pas encore de décoration libre, d'avatar riggé, de saisons synchronisées, de sauvegarde distante, de collisions complexes ni de système de récompenses définitif.
- Accès public en **démonstration seulement**, ne pas collecter de données personnelles sensibles.
- Pour une vraie V1 publique, Supabase Auth, RLS, uploads privés, politiques de confidentialité, tests Safari/Android physiques sont nécessaires.

## Contrôles

Ordinateur : clic sol, glisser pour pivoter, molette pour zoom, ZQSD / WASD / flèches pour avancer.

Téléphone : toucher pour avancer, glisser sur le décor pour pivoter, joystick à gauche, boutons de lieux et navigation en bas.
