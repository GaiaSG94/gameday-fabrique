# REFS — Fabrique

## V2 — base de l'usine, catégories `narratif-jeu` + `3d-matiere` (2026-11-18)

> Demande de Gaia après la V1 jugée « slop IA » : partir des refs design de l'usine (`hackatons-pipeline`, `REFERENCES-DESIGN.md` + `REFERENCES-CAPTURES/`). Les 21 captures des deux catégories ont été ouvertes. On prend des **principes**, jamais un layout, un texte, un asset ou une marque. Toutes les matières sont refaites en SVG/CSS embarqué (budget léger : aucune 3D temps réel).

### Retenues (2 par direction, catégories proches)

| Direction | Ref | Catégorie | Ce qu'on prend | Ce qu'on refuse |
|---|---|---|---|---|
| A Diorama | **Dairy Food Bulgaria** | narratif-jeu | Une scène miniature sur un îlot flottant dans les nuages qui raconte toute la chaîne de production d'un coup d'œil ; lumière douce venue d'en haut ; terre et roche sous le plateau | Le rendu photo-réaliste, l'herbe, les vaches, le produit-héros géant |
| A Diorama | **Matchball** | narratif-jeu | Des objets alignés sur un fond clair, chacun avec sa matière et son ombre de studio ; titre condensé très noir et très gros | Les ballons, le texte, l'alignement en frise horizontale pleine largeur |
| B Borne | **MemoryQuest** | narratif-jeu | Le jeu présenté comme un objet physique (borne) posé dans une pièce sombre avec un halo ; boutons ronds lumineux ; écran encastré | La borne d'arcade elle-même, le pixel art, le magenta/bleu |
| B Borne | **Igloo** | 3d-matiere | Des modules assemblés dont les joints s'éclairent ; petits libellés techniques sur fond froid | La scène 3D, le paysage, les blocs de glace |
| C Fonderie | **Yogi Suria** | 3d-matiere | Des objets-matière bruts qui flottent sur fond sombre ; une ligne de lumière rouge avec une mire au centre | Les astéroïdes, le rouge laser, la typo du portfolio |
| C Fonderie | **Primal Instinct** | 3d-matiere | La pierre sombre en relief comme surface ; petites capitales très espacées pour tout le méta | Le disque gravé, le lecteur audio, la navigation |

### Ouvertes, non retenues

- **Gapsy Studio** (lettres en relief + griffonnages) : seul le principe de l'annotation à la main est repris dans A (note « slot 04 »), pas les lettres 3D.
- **Raben Rifaie**, **Merci Studio**, **Gemeos**, **Don't Look Up**, **Funtech** : narration par le scroll, illustration de marque ou personnage, hors sujet pour un écran de jeu tenu dans un post.
- **Noon**, **Noddal**, **Defy the Current**, **Giallo**, **Köm**, **Framer**, **Psychoactive**, **Shutabug**, **Sponge** : 3D de décor ou produit-héros, non reproductible sans moteur 3D, ou trop proche d'une esthétique de landing page.

---

## V1 (archivée)

> Références ouvertes le 2026-11-18 (navigateur, page d'accueil + défilement complet). On prend des **principes**, jamais un layout, un texte, un asset ou une marque.

## Santalarch — santalarch.com

Observé :
- Fond quasi noir (≈ `#111111`) et bandes gris très clair (≈ `#efefef`), texte blanc ou noir pur. Aucune couleur : le contraste fait tout.
- La navigation est posée **sur une grille de colonnes apparente** : chaque rubrique commence sur une colonne, marquée par une petite graduation verticale sous le libellé, comme une cote sur un plan. Les colonnes restent visibles en filets 1 px sur tout le défilement.
- Le décor est du **dessin en fil de fer** : volumes de boîtes en perspective tracés à 1 px gris foncé, quelques arêtes rehaussées en blanc, des cotes minuscules le long des arêtes.
- Une seule grotesque neutre, très grande et fine pour les mots-clés, petite et serrée pour le reste. Préchargement minimal (une phrase centrée, un pourcentage).

À retenir pour Fabrique :
1. **La grille est visible et sert** : les emplacements de machines se posent sur des colonnes graduées, la graduation devient l'unité de temps.
2. **Le trait 1 px comme seul ornement** : machines dessinées au fil, pas de remplissage, pas d'ombre.
3. **Rehausser une arête** : l'élément actif est le seul trait plein et clair, le reste reste en sourdine.

## Baseten — baseten.co

Observé :
- Fond blanc posé sur une **trame de points** fine ; blocs à angles vifs (aucun arrondi), filets gris clair.
- Étiquettes de section en **mono capitales préfixées `::`** dans de petits pavés noirs ou teintés ; tout le méta (auteurs, légendes de chiffres) en mono capitales grises.
- Rangée de **chiffres-clés** : gros nombres en grotesque légère, légende mono dessous, séparés par des filets verticaux.
- Index à gauche : liste de libellés, l'actif en noir avec un petit carré plein, les autres en gris. Boutons pavés noirs pleine largeur avec une flèche ▸ à droite, secondaire en contour.
- Une couleur vive par bloc au plus, et seulement sur du contenu (citation, illustration), jamais sur la structure.

À retenir pour Fabrique :
1. **Hiérarchie froide** : un chiffre (le temps) en grand, le reste en mono petit. Lisible en 5 s.
2. **Densité d'outil** : chaque machine = une ligne de fiche (nom, entrée → sortie, durée), alignée en colonnes, sans carte décorative.
3. **Une seule action pleine** (« Run the line »), le reste en contour ou en texte.

## Ce qu'on n'emprunte pas

- Les polices propriétaires des deux sites ; on reste sur des familles système libres (Liberation Sans / DejaVu Sans Mono en repli), embarquables plus tard.
- Les volumes 3D animés de Santalarch, les illustrations isométriques et le vert de Baseten, leurs textes, leurs logos, leurs mises en page.
