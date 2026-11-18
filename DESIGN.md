# DESIGN — Fabrique (gameday-p22)

> Journal de design tenu par Claude (prompt design, `PROMPT-DESIGN.md`). Versions datées, jamais écrasées.
> Livrables dans `G-DESIGN/` : `PAGES.md`, `REFS.md`, `planches/v1/*.html` (STYLE.md viendra après validation du style).

## V2.1 — 2026-11-18 — style Diorama validé, déclinaison

**Statut : validé par Gaia le 2026-11-18 — les 4 pages (Jeu, Post, Carte de fin, Séries & classement) ont leur planche validée. Style verrouillé (`/lock`) le 2026-11-18.**

### Livré

- `G-DESIGN/STYLE.md` : palette (hex + matières en 3 tons), échelle typo, grille et cadre, composants, mouvement, règles d'états.
- `planches/v2/04-post.html` — **Post** (vue feed, desktop et mobile en contexte de fil) : îlot vide du jour, commande, 2 chiffres communautaires, bouton « Open the workshop » ; états déjà joué / première visite / chargement / série en danger.
- `planches/v2/05-carte-de-fin.html` — **Carte de fin** : « Spring delivered », atelier en marche et caisse pleine, étiquettes ton temps / meilleur temps, histogramme de la communauté, caisses de série, commentaire sans spoiler en un tap ; états trop lent / meilleure ligne / commentaire posté / chargement.
- `planches/v2/06-series-classement.html` — **Séries & classement** : lignes construites aujourd'hui (chaînes miniatures + part des joueurs), podium des plus longues séries + ton rang ; états onglet série (calendrier), pas encore joué (flou anti-spoiler), série cassée.

### Décisions

- Le cuivre désigne toujours « toi » (ton temps, ta ligne, ta série du jour) ou l'action principale ; onglet actif en encre pour ne pas concurrencer.
- Données de démo rendues cohérentes avec l'établi : seules 9:00 et 11:00 sont possibles aujourd'hui (23 % / 54 % / 23 % non terminé, 77 % sous 12:00).
- Le classement montre les séries plutôt que les temps (voir question 6 de `PAGES.md`).
- `01-diorama.html` (page Jeu) n'est pas retouchée : c'est la planche validée.

### Changelog

- 2026-11-18 — V2.1 : STYLE.md, planches Post, Carte de fin, Séries & classement.
- 2026-11-18 — V2.1 validée par Gaia (4/4 pages).
- 2026-11-18 — `/lock` : style Diorama verrouillé, fin des explorations.

## V2 — 2026-11-18 — refonte matière, refs narratif-jeu + 3d-matiere

**Statut : direction A Diorama retenue par Gaia ; B Borne et C Fonderie écartées.**

### Pourquoi une V2

Retour de Gaia sur la V1 : « slop IA », matière, couleurs et motifs non travaillés, pas d'identité visuelle. Diagnostic : les 3 planches V1 parlaient la grammaire d'un SaaS (filets 1 px, étiquettes mono, aplats), sans objet ni lumière. Consigne : s'appuyer sur les refs de l'usine, catégories `narratif-jeu` et `3d-matiere`.

### Livré

- `G-DESIGN/REFS.md` : section V2 (21 captures ouvertes, 6 retenues, principes pris et refusés).
- 3 nouvelles planches de la page Jeu, même état de démo que la V1, chacune avec desktop 1440 × 900, mobile 390 × 844 et 5 états :
  - `planches/v2/01-diorama.html` — **Diorama** (Dairy Food Bulgaria + Matchball) : l'atelier en miniature isométrique sur un îlot flottant, machines émaillées à pièces de cuivre, établi en objets sur socles, cadran de 12 minutes. Clair, cuivre comme seul accent.
  - `planches/v2/02-borne.html` — **Borne** (MemoryQuest + Igloo) : console d'atelier en acier brossé, afficheur à segments, 4 baies où l'on enfiche des cartouches (hublot = matière produite), joints et bouton RUN qui s'allument en ambre.
  - `planches/v2/03-fonderie.html` — **Fonderie** (Yogi Suria + Primal Instinct) : la matière en héros (minerai ▸ lingot ▸ fil ▸ bobine ▸ ressort) sur une ligne incandescente, mires de stations, pierre gravée, plaques de fonte embossées, horloge en métal en fusion.

### Décisions

- La matière vient du jeu : le cuivre et ses transformations sont l'identité commune aux 3 directions ; une seule couleur d'accent par direction (cuivre / ambre / braise).
- Tous les objets (machines isométriques, matières, LED, segments, pierre) sont dessinés en SVG et CSS dans le fichier : aucune image, aucune police ni requête externe.
- Polices système libres : Nimbus Sans Narrow Bold pour les titres condensés, Noto Sans pour le texte, Noto Serif Display pour C. À remplacer par des fontes OFL embarquées au build.
- Les planches V1 restent dans `planches/v1/` (versions jamais écrasées).

### Changelog

- 2026-11-18 — V2 : REFS V2, 3 planches matière de la page Jeu.

## V1 — 2026-11-18 — exploration du style sur la page Jeu

**Statut : rejetée par Gaia (2026-11-18, « slop IA ») — remplacée par la V2.**

### Compris du produit

Un atelier par jour, le même pour tout le monde : on reçoit une commande (une matière d'entrée, un produit à sortir) et on enchaîne 4 machines dont les entrées et sorties s'emboîtent. Chaque machine coûte du temps-machine ; la chaîne doit tenir sous 12:00, et le temps total sert de score. Fin de partie : temps, série, invitation à commenter.

### Livré

- `G-DESIGN/PAGES.md` : 4 pages proposées (Post, Jeu, Carte de fin, Séries & classement), données de démo de l'atelier 023, 5 questions produit ouvertes.
- `G-DESIGN/REFS.md` : Santalarch et Baseten ouverts et décodés (principes retenus, ce qu'on n'emprunte pas).
- 3 planches de la page Jeu, chacune avec cadre desktop 1440 × 900, cadre mobile 390 × 844 et une rangée d'états (vide, compatible, rejet, dépassement, chaîne lancée) :
  - `planches/v1/01-blueprint.html` — **Blueprint** : bleu plan `#0b2a4a`, trait `#7fb2d9`, alerte `#f2a65a` ; la chaîne en schéma de nœuds avec cotes de durée et liens pointillés. Direction de départ du brief.
  - `planches/v1/02-fiche.html` — **Fiche** : papier `#f4f4f0` sur trame de points, encre `#111214`, accent unique `#ff4d1a` ; la chaîne en tableau d'ordre de fabrication, une barre par machine sur l'échelle 0–12:00. S'écarte du brief.
  - `planches/v1/03-poste-de-nuit.html` — **Poste de nuit** : quasi-noir `#0f0f0f`, filets `#262626`, signal `#ffd23f` ; les 12 colonnes de la grille sont les 12 minutes, la chaîne posée sur une frise avec tête de lecture.

### Décisions

- Même état de jeu sur les 3 planches (3 machines posées, 7:30 engagées, emplacement 4 en aperçu) pour comparer le style, pas le contenu.
- Cadre hôte neutre (feed générique gris) : pas de logo ni de couleur de plateforme.
- Polices système libres uniquement (Liberation Sans, DejaVu Sans Mono) : rien à charger, compatible avec la CSP Devvit.
- Une seule couleur d'accent par direction, réservée à ce qui demande l'attention.
- Les planches s'ouvrent en double-clic ; elles se mettent à l'échelle de la fenêtre, ajouter `#1:1` à l'URL pour les voir en taille réelle.

### Hypothèses à confirmer (détail dans `PAGES.md`)

Sens de « recipe chaining », horloge = budget de temps-machine (pas du temps réel), 6 machines sur l'établi, nombre d'essais par jour, visibilité du meilleur temps pendant la partie.

### Changelog

- 2026-11-18 — V1 : PAGES, REFS, 3 planches de la page Jeu.
