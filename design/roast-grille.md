# M291 — Grille de roast — e2-1

**Nom :** Allan Sonzaï Heberling
**Date :** 30.10.2026
**Barème :** 1 = cassé · 3 = moyen · 5 = ça va (ces pages n'auront jamais 5 partout)

| Capture | Lisibilité | Navigation | Feedback | Cohérence | Accessibilité |
|---|---|---|---|---|---|
| **01 — Mur de texte** | 1 | 2 | 2 | 2 | 1 |
| **02 — Labyrinthe** | 3 | 1 | 2 | 2 | 2 |
| **03 — Silence** | 3 | 3 | 1 | 3 | 1 |
| **04 — Carnaval** | 2 | 3 | 2 | 1 | 1 |

## Phrases précises (2 par capture)

### 01 — Mur de texte
1. Le titre `h1`, le sous-titre `h2`, le paragraphe et les liens sont tous en 11 px, normal, `display: inline` : il n'y a aucune hiérarchie, l'œil ne sait pas par où commencer.
2. Le texte gris `#888` sur fond blanc donne un contraste d'environ 3,5:1, en dessous du minimum WCAG AA de 4,5:1, et le menu aligne 8 liens collés à 6 px d'écart, impossibles à viser au doigt.

### 02 — Labyrinthe
1. Le lien « Aide? » est placé en `position: absolute` à 70 % de la largeur, et le contenu commence à 40 % de la gauche : la page ne suit aucune grille ni ordre de lecture logique.
2. Le texte demande de passer par 6 niveaux (Menu > Espace > Plus > Options > Avancé > Liste) et avoue que « le bouton principal est quelque part » : il n'y a aucune action principale visible.

### 03 — Silence
1. Le bouton « ok » a le texte `#ddd` sur un fond `#ddd` : son libellé est invisible (contraste 1:1), et un clic ne produit rien du tout, ni message ni changement d'état.
2. Les champs « Email » et « Mot de passe » n'ont pas de `<label>` relié, et la mention « en cliquant vous acceptez tout » est en 11 px `#ccc` sur blanc (environ 1,6:1), donc illisible.

### 04 — Carnaval
1. Quatre polices différentes (Comic Sans, Impact, Georgia, Courier) et cinq couleurs vives (jaune, vert, rouge, bleu, magenta) cohabitent sur un seul écran : aucune identité cohérente.
2. La seule différence entre un prix promo et un prix normal est la couleur (rouge / vert) : une personne daltonienne ne voit pas la différence, et le texte vert `#0f0` sur jaune `#ff0` est quasiment illisible (environ 1,3:1).

## La pire, pour la présentation

**Capture n° 03 (Silence)** parce que c'est un formulaire de création de compte : c'est la page où l'utilisateur doit absolument réussir, et elle cumule les deux pires fautes, un bouton dont on ne peut pas lire le texte et un clic qui ne répond rien. L'utilisateur ne sait jamais si son compte est créé.

## Une correction mesurable par capture (pour les rapides)

| Capture | Correction mesurable |
|---|---|
| 01 | Le `h1` passe à 28 px gras, le corps à 16 px en `#333` (contraste 12,6:1), les liens du menu ont une hauteur de 48 px. |
| 02 | Le contenu suit une colonne unique alignée à gauche (marge 16 px) et le bouton principal « Voir la liste » apparaît en haut, en 48 px de haut. |
| 03 | Le bouton passe en fond `#1c1c1c` avec texte blanc (contraste 17:1) et affiche « Compte créé ✓ » pendant 2 secondes après le clic. |
| 04 | Une seule police (system-ui), fond blanc, et un badge texte « Promo » à côté de chaque prix réduit en plus de la couleur. |
