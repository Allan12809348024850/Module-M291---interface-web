# Tests utilisateurs et audit d'accessibilité — e2-7

**App testée :** Lêkê Sneakers (maquette Piste C, `propositions/piste-c-moderne.png`)
**Observateur :** Allan Sonzaï Heberling
**Testeur :** _à remplir (prénom du camarade)_
**Date du test :** _à remplir_

## 1. Protocole

**Scénario donné au testeur (1 phrase) :**
« Vous chaussez du 42 et vous avez 150 CHF : trouvez une paire qui vous plaît et ajoutez-la à vos favoris. »

**Règles pour moi, l'observateur :**
- Silence total : je ne guide pas, je ne justifie rien, je ne montre rien du doigt.
- Je demande au testeur de penser à voix haute (« dites tout ce que vous pensez »).
- Chronomètre lancé au moment où je lis le scénario, arrêt à 5 minutes maximum.
- C'est l'interface qui est testée, pas la personne.

## 2. Résultats du test

> À remplir pendant le test avec un camarade. Ne pas inventer : noter seulement ce qui a été vu et entendu.

**Test 5 secondes.** « C'est une appli pour… » (phrase exacte du testeur) :
_…_

**Temps pour accomplir la tâche :** _… min … s_ · **Réussi :** oui / non / avec aide

**Hésitations observées** (regard perdu, mauvais endroit touché, retour en arrière) :
- _…_
- _…_

**Remarques spontanées à voix haute :**
- « _…_ »
- « _…_ »

**J'ai aidé :** oui / non

## 3. Audit d'accessibilité

### Contrastes mesurés (norme WCAG AA : ≥ 4,5:1 pour le texte)

Mesures calculées avec la formule WCAG 2.1 (à vérifier avec WebAIM Contrast Checker).

| Élément | Couleurs | Ratio | AA |
|---|---|---|---|
| **Bouton principal « Filtrer »** | texte `#1c1c1c` sur `#ff6a13` | **5,94:1** | ✅ |
| Texte principal | `#1c1c1c` sur `#f6f4ef` | 15,50:1 | ✅ |
| Texte secondaire (marque, compteur) | `#5a5a5a` sur `#f6f4ef` | 6,27:1 | ✅ |
| Texte secondaire sur carte | `#5a5a5a` sur `#ffffff` | 6,90:1 | ✅ |
| En-tête | `#ffffff` sur `#1c1c1c` | 17,04:1 | ✅ |
| Message d'erreur | `#b3261e` sur `#ffffff` | 6,54:1 | ✅ |
| ⚠️ Orange en couleur de texte | `#ff6a13` sur `#f6f4ef` | 2,61:1 | ❌ → interdit |
| ⚠️ Texte blanc sur orange | `#ffffff` sur `#ff6a13` | 2,87:1 | ❌ → interdit |

### Navigation au clavier (Tab / Entrée, sans souris)

À vérifier sur la version codée (`index.html`) :

| Vérification | Résultat |
|---|---|
| Tab atteint la recherche, les filtres, chaque carte et chaque cœur dans l'ordre visuel | _…_ |
| Le focus est toujours visible (contour net) | _…_ |
| Entrée / Espace active les boutons « Filtrer » et « favori » | _…_ |
| Aucune action n'est possible uniquement à la souris | _…_ |

### Cibles tactiles

Toutes les zones cliquables de la maquette (puces, « Filtrer », cœurs, recherche) font au moins 48 × 48 px. ✅

## 4. Deux correctifs prioritaires

> À confirmer ou remplacer après le test : chaque correctif doit venir d'une friction observée.

1. **Feedback favoris.** Avant : le cœur reste identique après le clic. Après : cœur plein + message « Ajoutée aux favoris » affiché 2 secondes, et le compteur de favoris dans l'en-tête passe de 0 à 1.
2. **Filtres visibles.** Avant : les filtres sont des menus fermés « Pointure ▾ » / « Prix max ▾ ». Après : une fois choisis, ils deviennent des puces actives « Pointure 42 ✕ » / « ≤ 150 CHF ✕ » avec le nombre de résultats et un lien « Réinitialiser » (voir `wireframes/02-recherche-filtre.png`).
