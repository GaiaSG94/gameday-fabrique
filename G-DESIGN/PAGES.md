# PAGES — Fabrique

> Statuts : à dessiner / en revue / validée. Liste de départ du brief, **à valider par Gaia**.
> Chaque planche montre le cadre desktop 1440 × 900 et le cadre mobile 390 × 844 côte à côte.

| # | Page | Rôle | Contenu clé | Statut |
|---|------|------|-------------|--------|
| 1 | **Post** | Vue dans le feed : donner envie d'ouvrir l'atelier du jour | En-tête du post, n° de l'atelier, commande du jour (matière d'entrée ▸ produit), nombre de joueurs du jour, série du joueur, bouton « Open the workshop » | **validée (2026-11-18)** — `planches/v2/04-post.html` |
| 2 | **Jeu** | Écran principal, une seule règle : « Ore in, spring out — 4 machines, under 12:00 » | Commande du jour, horloge 12:00 (temps engagé / budget), chaîne de 4 emplacements reliés, établi de machines (entrée → sortie, durée), bouton « Run the line » | **validée (style Diorama, 2026-11-18)** — `planches/v2/01-diorama.html` |
| 3 | **Carte de fin** | Résultat + boucle quotidienne + accroche commentaire | Temps de la chaîne vs 12:00, comparaison à la meilleure chaîne du jour, série, % de la communauté sous 12:00, schéma de la chaîne partageable sans spoiler, bouton commenter, prochain atelier dans HH:MM | **validée (2026-11-18)** — `planches/v2/05-carte-de-fin.html` |
| 4 | **Séries & classement** | Montrer la communauté et la série | Série perso (calendrier), classement du jour (temps de chaîne), répartition des chaînes construites par la communauté | **validée (2026-11-18)** — `planches/v2/06-series-classement.html` |

## Données de démo utilisées (atelier 023, mer. 18 nov.)

Commande : **copper ore ▸ spring**, 4 machines, budget 12:00.

| Machine | Entrée → sortie | Durée |
|---|---|---|
| Smelter | ore → ingot | 3:00 |
| Wire drawer | ingot → wire | 2:30 |
| Roller | ingot → sheet | 1:30 |
| Coiler | wire → coil | 2:00 |
| Curler | sheet → coil | 1:00 |
| Temper oven | coil → spring | 3:30 |

- Chaîne « évidente » : Smelter ▸ Wire drawer ▸ Coiler ▸ Temper oven = **11:00** (sous le budget).
- Chaîne « fine » : Smelter ▸ Roller ▸ Curler ▸ Temper oven = **9:00** (meilleur temps du jour).
- État dessiné sur la planche Jeu : 3 machines posées (7:30 engagées), l'emplacement 4 en aperçu.

## Questions produit ouvertes (non tranchées, `IDEE.md` ne dit rien)

1. **Que veut dire « recipe chaining » exactement ?** Les planches supposent : chaque machine transforme une matière A en B en un temps donné ; on pose 4 machines dont les sorties et entrées s'emboîtent, de la matière d'entrée au produit demandé. À confirmer.
2. **L'horloge de 12 minutes est-elle du temps de jeu (somme des durées des machines) ou du temps réel ?** `IDEE.md` impose une partie < 2 min, donc les planches la dessinent comme un **budget de temps-machine** : le score = durée totale de la chaîne, plus bas = mieux. À confirmer.
3. **Combien de machines sur l'établi ?** Les planches en montrent 6 (le « 6 salles max » des risques), dont des leurres. À confirmer.
4. **Un seul essai par jour ou plusieurs ?** Les planches ne montrent ni essais ni pénalité : on construit, puis « Run the line » valide. À trancher avant la carte de fin.
5. **Le meilleur temps de la communauté est-il visible pendant la partie ?** Les planches ne le montrent qu'en fin de partie (pas de spoiler) ; en jeu, seulement le nombre de joueurs du jour et la série.
6. **Classement : par temps ou par série ?** Avec un établi de 6 machines, peu de chaînes sont possibles (aujourd'hui seulement 9:00 et 11:00) : un classement au temps serait plein d'égalités. La planche Séries & classement montre donc la répartition des lignes construites + le classement des plus longues séries. Faut-il un départage (temps réel de construction) ?
7. **Chaîne au-delà de 12:00 : fin de partie ou résultat dégradé ?** La carte de fin suppose que la partie compte (série conservée) avec un titre « Line too slow ».
8. **« Post my time »** publie un commentaire au nom du joueur en un tap (texte affiché à l'écran, sans la chaîne). À confirmer côté Devvit (commentaire au nom de l'utilisateur vs de l'app).
