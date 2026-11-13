# Contrôle du prototype de suivi de stock — 13 novembre 2026

## Résultat de cette session

Un nouveau prototype ODS v2.0 a été créé localement et recalculé avec LibreOffice Calc en mode sans interface. Deux fichiers ont été produits pour le travail interne :

- `Tableaux_Methodes_Suivi_Stock_demo_v2_0.ods` : exemples entièrement fictifs.
- `Tableaux_Methodes_Suivi_Stock_vierge_v2_0.ods` : version sans références ni mouvements d'exemple.

Les deux fichiers contiennent cinq feuilles : Guide, Mouvements, Stock, Tableau de bord et Listes. Chacun contient 406 cellules de formule : quatre calculs par ligne de stock sur 100 références, plus six indicateurs de tableau de bord. Les plages du journal couvrent 500 mouvements.

Les fichiers binaires ne sont pas ajoutés au dépôt public : ils restent des prototypes de travail et ne sont pas proposés à la livraison commerciale.

## Tests recalculés

### Données de démonstration

| Article | Stock initial | Entrées | Sorties | Stock calculé | Seuil | Alerte |
|---|---:|---:|---:|---:|---:|---|
| Gants nitrile | 10 | 0 | 2 | 8 | 10 | À COMMANDER |
| Nettoyant | 20 | 10 | 6 | 24 | 8 | OK |
| Joint 20 mm | 5 | 0 | 2 | 3 | 5 | À COMMANDER |

Tableau de bord recalculé : 3 références, 2 articles à commander, 0 stock négatif, 1 article au-dessus du seuil, 4 mouvements et 35 unités au total.

### Cas dynamiques

| Modification temporaire | Stock recalculé | Alerte | Résultat |
|---|---:|---|---|
| Sortie des gants portée à 7 | 3 | À COMMANDER | Réussi |
| Stock exactement égal au seuil | 10 | À COMMANDER | Réussi |
| Sortie des gants portée à 15 | -5 | STOCK NÉGATIF | Réussi |

Les essais ont été effectués sur des copies temporaires, puis les fichiers de base ont été conservés avec les exemples initiaux.

### Version vierge

Après recalcul : 0 référence, 0 mouvement, 0 alerte, 0 stock négatif et 0 unité. Les formules restent présentes sur les plages prévues.

## Limites non levées

- Les filtres ne sont pas préconfigurés ; ils doivent être activés dans Calc.
- Les listes de valeurs sont présentes, mais les menus déroulants ne sont pas encore configurés.
- La saisie de quantités négatives n'est pas bloquée.
- Les références en double et les références de mouvement inconnues ne déclenchent pas encore de contrôle dédié.
- Le rendu visuel et la navigation dans une session LibreOffice Calc avec interface n'ont pas encore été vérifiés.
- La compatibilité Microsoft Excel n'a pas été testée.

## Décision produit

**Prototype technique vérifié, mais pas encore produit commercial prêt à livrer.** Le site doit conserver le statut « en préparation » jusqu'à la vérification visuelle et à la finalisation des contrôles de saisie.

## Prochaine priorité

1. Ouvrir les deux ODS dans LibreOffice Calc avec interface et vérifier largeur des colonnes, lisibilité, filtres et impression.
2. Ajouter des listes déroulantes et validations pour le type de mouvement, les catégories et les quantités.
3. Ajouter des contrôles de références inconnues et en double.
4. Rejouer les tests après chaque modification, puis préparer une version client vierge et une démonstration publique allégée.
