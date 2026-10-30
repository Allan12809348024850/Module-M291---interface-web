# Critique comparative et arbitrage — e2-6

**App :** Lêkê Sneakers · **Écran comparé :** Accueil (liste + filtres) · **Date :** 30.10.2026

Les trois pistes utilisent le même contenu et la même structure que le wireframe `wireframes/01-accueil-mobile.png`. Seule la direction artistique change.

| Piste | Capture |
|---|---|
| A — Éditoriale & sobre | `propositions/piste-a-editoriale.png` |
| B — Chaleureuse | `propositions/piste-b-chaleureuse.png` |
| C — Moderne & pragmatique | `propositions/piste-c-moderne.png` |

## Matrice d'évaluation (1 = cassé · 5 = ça va)

| Critère | Piste A | Piste B | Piste C |
|---|---|---|---|
| Lisibilité | 3 | 4 | 5 |
| Navigation | 3 | 4 | 5 |
| Feedback | 3 | 3 | 4 |
| Cohérence | 4 | 4 | 4 |
| Accessibilité | 4 | 3 | 4 |
| **Total / 25** | **17** | **18** | **22** |

## Fiches critiques

### Piste A — Éditoriale & sobre (serif, blanc chaud, bleu nuit)

**2 forces**
1. Accessibilité — preuve : le bouton « Filtrer » bleu nuit `#1e2a44` sur blanc chaud `#faf8f3` atteint 13,5:1.
2. Cohérence — preuve : une seule couleur d'accent et des filets fins répétés partout, l'ensemble fait « catalogue de magazine ».

**2 faiblesses**
1. Lisibilité — preuve : le prix en Georgia 20 px normal ne ressort pas plus que le nom du modèle ; Noah doit chercher le prix, alors que c'est son critère n° 1.
2. Navigation — preuve : le cœur des favoris n'a ni bordure ni fond, il ne ressemble pas à un bouton touchable.

**Verdict :** j'**élimine** cette piste : l'ambiance « magazine chic » ne parle pas à un apprenti de 17 ans qui cherche une paire à moins de 150 CHF dans le bus.

### Piste B — Chaleureuse (formes rondes, sauge, terracotta)

**2 forces**
1. Navigation — preuve : puces de filtre et bouton « Filtrer » en pilules de 48 px de haut, faciles à toucher d'une main.
2. Lisibilité — preuve : le prix est en gras et en terracotta, il se repère tout de suite sur la carte (4,9:1 sur la carte).

**2 faiblesses**
1. Accessibilité — preuve : la marque en vert sauge `#8a9a7b` sur la carte `#fffdf8` ne fait que 3:1, sous le minimum de 4,5:1.
2. Cohérence avec le brief — preuve : le brief demande « jeune, énergique, épuré, un seul accent orange vif » ; la piste B est douce et posée, elle évoque plutôt une marque de produits bio.

**Verdict :** j'**élimine** cette piste comme direction principale, mais je garde l'idée des grandes zones tactiles arrondies.

### Piste C — Moderne & pragmatique (sans serif grasse, noir, accent orange)

**2 forces**
1. Lisibilité — preuve : le prix est le texte le plus gros de la carte (22 px, graisse 900), le texte principal noir `#1c1c1c` sur `#f6f4ef` atteint 15,5:1.
2. Navigation — preuve : le seul élément orange de l'écran est le bouton « Filtrer », donc l'action principale du brief saute aux yeux ; toutes les cibles font au moins 48 × 48 px.

**2 faiblesses**
1. Accessibilité — preuve : l'orange `#ff6a13` ne doit jamais servir de couleur de texte sur le fond clair (2,6:1) ni porter un texte blanc (2,9:1) ; il marche uniquement avec du texte noir (5,9:1).
2. Feedback — preuve : sur la maquette statique, rien n'indique l'état « ajouté aux favoris » ; il faut prévoir un cœur plein + message.

**Verdict :** je **garde** ce design parce que Noah veut voir prix et pointure en un coup d'œil, d'une main, et que c'est la seule piste qui colle à l'ambiance « vitrine de magasin de sneakers » du brief.

## Arbitrage

Je retiens la **Piste C (Moderne & pragmatique)** pour son adéquation avec le persona et le brief : prix en très gros, un seul accent orange réservé à l'action principale, contrastes au-dessus de 4,5:1 sur tous les textes. J'y intègre les **coins arrondis et les grandes zones tactiles de la Piste B** pour adoucir un peu le rendu, et deux règles d'accessibilité :

1. l'orange `#ff6a13` porte toujours du texte noir `#1c1c1c`, jamais du blanc, et n'est jamais utilisé comme couleur de texte ;
2. l'état « favori » est montré par un cœur plein **et** un message texte « Ajoutée aux favoris », pas seulement par la couleur.

## Palette retenue (hex)

| Rôle | Couleur | Hex |
|---|---|---|
| Fond | blanc cassé | `#f6f4ef` |
| Surface (cartes) | blanc | `#ffffff` |
| Texte | noir charbon | `#1c1c1c` |
| Texte secondaire | gris | `#5a5a5a` (6,3:1 sur le fond) |
| Accent | orange vif | `#ff6a13` (avec texte noir, 5,9:1) |
| Attention / erreur | rouge brique | `#b3261e` (6,5:1 sur blanc) |
