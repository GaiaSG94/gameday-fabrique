# STYLE — Fabrique · Diorama

> **Style verrouillé le 2026-11-18 (`/lock`)** : fin des explorations ; toute évolution passe par `/delta` sur une page existante.
> Style validé par Gaia le 2026-11-18 (V2, direction A « Diorama », planche `planches/v2/01-diorama.html`).
> Refs : Dairy Food Bulgaria + Matchball (voir `REFS.md`). Toute nouvelle page reste dans ce cadre ; pas d'empilement de styles.

## 1. Idée

L'atelier du jour est un **jouet** : une usine miniature isométrique posée sur un îlot flottant, vue de haut à gauche, sous une lumière de studio douce. Le joueur manipule des objets, pas des composants d'interface. **Le cuivre est à la fois la matière du jeu et la seule couleur d'accent** : ce qui est cuivre, c'est ce qui avance, ce qui est à toi, ce qui demande ton geste.

## 2. Palette

| Rôle | Hex | Usage |
|---|---|---|
| Ciel | `#f3eee5` (dégradé radial `#fbf8f2` → `#e6ddcd`) | Fond de toutes les vues + grain papier (bruit SVG, multiply 50 %) |
| Encre | `#1f1c18` | Titres, texte, traits de marquage au sol |
| Gris atelier | `#8a8275` | Texte secondaire, libellés, états inactifs |
| Filet | `#cbbfae` | Contours de boutons secondaires, socles inactifs |
| **Cuivre** | `#c8642c` (clair `#e2874d`, ombre `#8f4219`) | Seul accent : bouton principal, slot à remplir, ton résultat, ta ligne au classement, annotations |
| Cuivre pâle | `#f2c7a6` | Projection (temps prévu, fantômes), fond de socle « compatible » |

Matières (3 tons chacune, lumière haut-gauche : dessus / face éclairée / face d'ombre) :

| Matière | Dessus | Face +y | Face +x |
|---|---|---|---|
| Émail (machines) | `#f6f1e7` | `#ddd3c2` | `#b9ad9a` |
| Cuivre | `#f0a873` | `#c8642c` | `#8f4219` |
| Acier | `#d7dbde` | `#a8afb5` | `#7c848b` |
| Bordure (socles machine) | `#4a453f` | `#33302b` | `#25221f` |
| Caoutchouc (tapis) | `#55524d` | `#3a3834` | `#2a2825` |
| Béton (plateau) | `#ece6da` | `#d3c9b8` | `#b8ab96` |
| Terre / roche (sous l'îlot) | `#c9ab86` → `#5e4a39` | | |
| Bois (caisse) | `#d9b07c` | `#b98a55` | `#93683c` |
| Incandescent | `#fff1c2` → `#ffb04a` → `#e2541c` | | Uniquement dans les fours (lumière, pas de l'UI) |

Interdits : toute autre teinte saturée ; dégradés décoratifs hors matières ; noir pur ; blanc pur en grand aplat (le blanc pur est réservé aux étiquettes et aux reflets).

## 3. Typographie

Une seule échelle, deux familles (fontes système pour les planches ; au build, embarquer des équivalents OFL, ex. une grotesque condensée bold + une sans humaniste).

| Niveau | Famille | Taille / interligne | Usage |
|---|---|---|---|
| Display | Nimbus Sans Narrow Bold, capitales | 50 / 0.9 (mobile 34) | Commande du jour, résultat (« SPRING DELIVERED ») |
| Titre | Nimbus Sans Narrow Bold, capitales | 16–24 / 1 | Noms de machines, titres de blocs, boutons |
| Chiffre | Nimbus Sans Narrow Bold | 26–64 | Temps, rangs, pourcentages |
| Texte | Noto Sans 400/600 | 13 / 1.45 (mobile 11) | Phrases, consignes |
| Libellé | Noto Sans 600–700, capitales, +.08em | 9–11 | Pastilles, légendes |
| Annotation | Nimbus Sans Narrow Bold italique, cuivre | 15–16 | Notes « à la main » (une par écran maximum) |

## 4. Grille et cadre

- Post Devvit : desktop 736 px de large dans le feed, mobile 390 px. Marges intérieures 22 px (desktop) / 14 px (mobile).
- Composition fixe : **en-tête** (marque + pastilles) en haut, **titre display** en haut à gauche, **cadran** en haut à droite, **scène** au centre, **établi / actions** en bas. Les pages hors-jeu gardent cette structure (titre en haut à gauche, objet-héros au centre, action cuivre en bas à droite).
- Isométrie : 30°, unité 28 px desktop (13–16 px pour les vignettes), lumière haut-gauche, ombres portées vers le bas-droite (flou 4 px, `#2b2017` à 18–22 %).

## 5. Composants

| Composant | Description |
|---|---|
| **Îlot** | Plateau béton 14,9 × 4 unités, épaisseur terre, dessous rocheux irrégulier, nuages flous blancs autour |
| **Socle peint** | Rectangle pointillé 5/4 au sol, numéro peint au sol (01–04). Cuivre et 1,6 px pour le slot à remplir |
| **Machine** | Jouet isométrique sur base sombre, carrosserie émail, pièce caractéristique en cuivre ou acier (6 modèles : Smelter, Wire drawer, Roller, Coiler, Curler, Temper oven) |
| **Étiquette suspendue** | Carte papier 92 × 36, trou d'œillet, fil vers la machine, légère rotation ±2–3°, n°, nom, durée. Version fantôme : pointillé cuivre |
| **Objet sur socle** | Vignette de machine posée sur un socle elliptique (établi, classement). Compatible : soulevé de 10 px, socle cuivré |
| **Cadran 12 min** | Disque crème, 24 graduations, secteur cuivre plein = temps engagé, secteur cuivre pâle = projeté, chiffre au centre |
| **Pastille** | Pilule blanche translucide, ombre douce, valeur en cuivre si elle concerne le joueur |
| **Bouton principal** | Pilule cuivre en relief (ombre pleine 5 px `#8f4219`), capitales condensées. Inactif : émail avec ombre `#cbbfae` |
| **Bouton secondaire** | Contour 1,5 px `#cbbfae`, texte encre, sans relief |
| **Annotation** | Trait à main levée cuivre + texte italique condensé ; jamais de toast |

## 6. Mouvement

- Poser une machine : chute de 12 px + rebond (ressort 220 ms), l'ombre se resserre.
- Survol / sélection d'un objet compatible : il se soulève de 10 px (160 ms ease-out), l'ombre s'étire.
- Rejet : rebond sur place et retour à l'établi, annotation manuscrite pendant 1,6 s.
- Chaîne lancée : les objets roulent sur les tapis machine par machine (minerai → lingot → fil → bobine → ressort), 400 ms par étape, puis la caisse se remplit.
- Cadran : les secteurs se remplissent en 300 ms à chaque changement.
- Respecter `prefers-reduced-motion` : fondus seuls.

## 7. Règles d'états

| État | Rendu |
|---|---|
| Vide | Socle pointillé + ce qu'il attend (« needs coil in ») |
| Compatible | Objet soulevé, socle cuivré, pastille « fits 04 » |
| Incompatible | Objet désaturé à 30 % d'opacité, sans pastille |
| Déjà utilisé | Objet à 42 %, pastille contour « in line » |
| Rejet | Rebond + annotation cuivre, aucun rouge |
| Dépassement | Cadran bouclé, couronne pointillée cuivre, bouton inactif |
| Terminé | Caisse pleine, secteurs pleins, résultat en display |
| Chargement | L'îlot se construit (plateau, puis socles, puis machines) en 600 ms |
