# Lêkê Sneakers

Projet du module ICT 291 (Développer des interfaces utilisateurs), réalisé au CPNV par **Allan Sonzaï Heberling**, en médiamatique.

## Présentation

Lêkê Sneakers est un site vitrine pour trouver rapidement une paire de sneakers selon sa pointure et son budget. Il s’adresse aux jeunes en Suisse romande, sur smartphone, sans compte à créer et sans paiement.

Le dossier design (Note 1) est en place : pitch, persona, user flow, brief, wireframes, 3 directions graphiques, critique et protocole de tests. L’écran d’accueil est codé en HTML/CSS (s9) et la base de données `data.json` (32 paires) est prête (s10) ; le chargement avec `fetch`, la recherche et les favoris arrivent dans les prochaines semaines.

## Objectifs

- Concevoir une interface **simple, lisible et rapide** sur mobile (écran de référence : 390 px)
- Afficher une liste de sneakers sous forme de cartes, avec filtre par pointure et prix
- Proposer une fiche détail et des favoris, avec une confirmation visuelle immédiate
- Respecter l’accessibilité (contrastes WCAG AA, navigation au clavier)
- Apprendre à utiliser Git et GitHub

## Technologies utilisées

1. HTML5 sémantique
2. CSS moderne (variables CSS)
3. JavaScript natif, sans bibliothèque
4. Git
5. GitHub

Aucun framework : pas de Bootstrap, pas de React.

## Structure du dépôt

```
├── README.md
├── index.html              Écran d’accueil de l’app (s9)
├── style.css               Design tokens + mise en page mobile first
├── js/app.js               Vide pour l’instant (fetch en s11)
├── data.json               Catalogue : 32 paires typées (e3-2)
├── data/
│   ├── schema.json         Schéma de validation JSON Schema (s10-av1)
│   ├── data-avance.json    Magasins avec GPS et horaires (s10-av2)
│   └── README.md           Description des champs
├── presentation.html       Ma page de présentation
├── brief.md                Brief client du projet
├── kit-ia.md               Mes outils IA
└── design/
    ├── pitch.md            Pour qui, quel besoin, quelle réponse
    ├── persona.md          Noah, 17 ans, apprenti
    ├── user-flow.md        Parcours en 5 étapes
    ├── roast-grille.md     Grille de roast e2-1
    ├── wireframes/         3 wireframes mobiles basse fidélité (e2-4)
    ├── propositions/       3 directions graphiques A / B / C (e2-5)
    ├── critique.md         Critique comparative et choix de la piste C (e2-6)
    └── tests-utilisateurs.md  Protocole de test + audit accessibilité (e2-7)
```

## Installation

Pour récupérer le projet :

```bash
git clone https://github.com/Allan12809348024850/Module-M291---interface-web.git
```

Ouvre ensuite le dossier dans VS Code. Il n’y a rien à installer : le site se lance en ouvrant `index.html` dans un navigateur.

## Journal IA

| Date | Outil | Prompt (résumé) | Ce que j’ai corrigé à la main |
|---|---|---|---|
| 30.10.2026 | Claude | « Voici mon brief et mon wireframe : génère 3 directions artistiques (éditoriale, chaleureuse, moderne) en HTML5 sémantique et CSS avec variables, sans framework. » | J’ai choisi la piste moderne : le site vise les jeunes, il doit être facile à comprendre et à naviguer, dans l’esprit des sites de sneakers qui m’ont inspiré. |
| 30.10.2026 | Claude | « Calcule les ratios de contraste WCAG de ma palette et dis-moi quelles combinaisons sont interdites. » | Validé : l’orange sert seulement de fond aux boutons, jamais de couleur de texte. J’ai gardé l’orange et le beige, qui sont aussi les couleurs de mon e-portfolio. |
| 30.10.2026 | Claude | « Intègre l’écran d’accueil de la piste C en mobile first avec une media query à 768 px. » | Validé comme base. Changements que je veux faire : un menu de navigation par couleur et par style, une fiche détail au clic sur une paire (description et choix de la pointure), et une intro qui explique pourquoi choisir Lêkê Sneakers. |
| 06.11.2026 | Claude | « Crée data.json avec au moins 30 sneakers typées, puis le schéma de validation et l’échantillon avec GPS et horaires des ateliers avancés. » | Pas encore de correction : les paires ne sont pas encore affichées sur le site. Je les relirai quand elles seront affichées avec leurs images. |
