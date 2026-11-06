# Données de Lêkê Sneakers

- `../data.json` : le catalogue officiel (32 paires), chargé par l'app avec `fetch` à partir de s11.
- `schema.json` : schéma JSON Schema draft-07 qui valide `data.json` (atelier s10-av1).
- `data-avance.json` : échantillon de 3 paires avec un magasin imbriqué, ses coordonnées GPS et ses horaires (atelier s10-av2).

## Structure d'une paire (`data.json`)

| Champ | Type | Obligatoire | Exemple |
|---|---|---|---|
| `id` | entier ≥ 1, unique | oui | `1` |
| `marque` | texte | oui | `"Kova"` |
| `modele` | texte | oui | `"Runner Lac 2"` |
| `categorie` | `running`, `lifestyle`, `basket`, `skate` ou `trail` | non | `"running"` |
| `couleur` | texte | non | `"blanc / gris"` |
| `description` | texte, 160 caractères max. | non | `"Running léger…"` |
| `prix` | nombre en CHF, entre 0 et 160 | oui | `129.00` |
| `enStock` | booléen | oui | `true` |
| `pointures` | tableau d'entiers entre 35 et 47, sans doublon | oui | `[40, 41, 42]` |
| `tags` | tableau de textes | non | `["léger", "amorti"]` |
| `magasin` | ville du magasin en Suisse romande | non | `"Lausanne"` |
| `image` | chemin vers `images/` (.webp, .jpg ou .png) | non | `"images/kova-runner-lac-2.webp"` |

Le prix est plafonné à 160 CHF, parce que l'accroche du site promet des sneakers à moins de 160 CHF.

## Données avancées (`data-avance.json`)

`magasin` y devient un objet :

- `coordonnees` : `{ "lat": …, "lng": … }`, en degrés décimaux, pour une future carte.
- `horaires` : un tableau de plages `{ "ouverture", "fermeture" }` par jour. Un tableau vide veut dire fermé ; deux plages, c'est une pause de midi.

## Valider

Dans VS Code, `data.json` est vérifié par le schéma grâce au réglage `json.schemas` de `.vscode/settings.json` : une erreur s'affiche en rouge directement dans le fichier.
Sinon, coller les deux fichiers sur https://www.jsonschemavalidator.net/.

Les marques et les magasins sont fictifs.
