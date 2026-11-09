# Journal de tests — Suivi de stock ODS v2.1

**Date :** 9 novembre 2026  
**Application de contrôle :** LibreOffice (recalcul ODS)  
**Fichier :** Tableaux_Methodes_Suivi_Stock_v2_1.ods  
**Feuilles :** Guide, Mouvements, Stock, Tableau de bord, Listes  
**Formules :** 405  
**Capacité préconfigurée :** 100 références, 500 mouvements

## Tests statiques sur les exemples fictifs

| Cas | Entrées | Sorties | Stock initial | Stock calculé | Seuil | Alerte |
|---|---:|---:|---:|---:|---:|---|
| Gants nitrile | 0 | 2 | 10 | 8 | 10 | À COMMANDER |
| Nettoyant | 10 | 6 | 20 | 24 | 8 | OK |
| Joint 20 mm | 0 | 2 | 5 | 3 | 5 | À COMMANDER |

Tableau de bord contrôlé : 3 références, 2 articles à commander, 1 article au-dessus du seuil, 4 mouvements, 35 unités au total.

## Tests dynamiques

| Modification du journal | Stock recalculé | Alerte | Résultat |
|---|---:|---|---|
| Sortie des gants modifiée de 2 à 7 | 3 | À COMMANDER | Réussi |
| Sortie des gants modifiée à 0 (stock exactement égal au seuil) | 10 | À COMMANDER | Réussi |
| Sortie des gants modifiée à 15 (stock négatif) | -5 | STOCK NÉGATIF | Réussi |

Les tests dynamiques ont été effectués sur des copies temporaires du classeur ; le fichier de base conserve les exemples initiaux.

## Vérifications structurelles

- Les cinq feuilles sont présentes et le fichier ODS se rouvre après recalcul.
- Les lignes vides prévues ne sont pas comptées dans les indicateurs.
- Les plages de filtres Stock et Mouvements sont présentes dans le fichier ODS.
- Les listes de catégories, types et motifs sont présentes dans l'onglet Listes.
- Aucune donnée réelle de client n'est utilisée.

## Limites restantes

- Le fonctionnement visuel des filtres doit encore être contrôlé dans une session LibreOffice avec interface.
- Les listes ne sont pas des menus déroulants : aucune validation de données n'est encore appliquée.
- Les quantités négatives ne sont pas bloquées à la saisie.
- Les références inconnues ou en double ne sont pas automatiquement détectées.
- La compatibilité Excel n'a pas été testée.
- Un test utilisateur non technique reste à réaliser.

**Conclusion :** les calculs de base et les alertes du modèle ODS v2.1 passent les tests documentés dans LibreOffice. Le fichier est un modèle de travail fonctionnel pour Calc, mais les limites ci-dessus doivent être prises en compte avant une diffusion commerciale plus large.
