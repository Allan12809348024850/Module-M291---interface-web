# Brief — Lêkê Sneakers

## Pitch

Lêkê Sneakers est un site vitrine pour trouver rapidement une paire de sneakers selon sa pointure et son budget. Il s’adresse aux jeunes en Suisse romande, sur smartphone, sans compte à créer.

## Public

Noah Rochat, 17 ans, apprenti près de Lausanne. Il navigue d’une main sur son téléphone (390 px), souvent dans les transports. Son budget est serré : il veut voir prix et pointures tout de suite et ferme l’onglet si on lui demande un compte. Détails dans `design/persona.md`.

## Écrans

- Écran 1 : Accueil (liste des sneakers)
- Écran 2 : Filtrage (pointure et prix)
- Écran 3 : Fiche détail d’une paire
- Écran 4 : Favoris (confirmation et liste)

## Contenu de chaque écran

### Écran 1 — Accueil
- On y voit : le nom de l’app, une phrase d’accroche, la liste des 12 sneakers en cartes (photo, modèle, prix en CHF) et l’accès aux filtres.
- On peut y faire : parcourir la liste, ouvrir les filtres, ouvrir une carte.
- Bouton principal : « Filtrer ».

### Écran 2 — Filtrage
- On y voit : le choix de la pointure, un prix maximum, le nombre de résultats qui se met à jour en direct.
- On peut y faire : choisir une pointure et un prix, réinitialiser les filtres.
- Bouton principal : « Voir les résultats ».

### Écran 3 — Fiche détail
- On y voit : une grande photo, le modèle, la marque, le prix en CHF, les pointures disponibles, la couleur et une courte description.
- On peut y faire : revenir à la liste, ajouter la paire aux favoris.
- Bouton principal : « Ajouter aux favoris ».

### Écran 4 — Favoris
- On y voit : un message de confirmation (« Ajoutée aux favoris ») et la liste des paires enregistrées.
- On peut y faire : retirer une paire des favoris, retourner à la liste.
- Bouton principal : « Continuer à explorer ».

## Ambiance visuelle

Jeune, énergique, épuré. Comme la vitrine d’un magasin de sneakers : peu de texte, de grandes photos, un seul accent de couleur qui attire l’œil.

## Palette

- Fond : blanc cassé
- Texte : noir charbon
- Accent : orange vif
- Attention / erreur : rouge brique

(Couleurs en mots pour l’instant ; hex en s7-s9.)

## Interdits

- pas de Bootstrap, pas de React, pas de compte obligatoire pour consulter
- pas de popup de newsletter ni de bannière envahissante à l’arrivée
- pas de panier ni de paiement (site vitrine uniquement)
