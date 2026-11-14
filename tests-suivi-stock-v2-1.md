# Journal de tests — Suivi de stock ODS v2.1

> **Disponibilité du binaire vérifiée le 12 novembre 2026 : fichier non retrouvé.** Ce document conserve la trace des tests consignés le 9 novembre, mais le classeur `Tableaux_Methodes_Suivi_Stock_v2_1.ods` n'est pas présent dans le dépôt public ni dans les fichiers accessibles pendant ce contrôle. Les résultats ci-dessous sont donc un historique de tests rapportés, pas une validation que l'on peut rejouer aujourd'hui ni un fichier disponible à livrer. La maquette v1 jointe précédemment n'est pas automatisée.

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


## Reconstruction et contrôle complémentaire — 14 novembre 2026

Le binaire ODS v2.1 a été reconstruit localement à partir du prototype v2.0 remis dans la conversation. Deux fichiers sont présents dans l'espace de travail : une démonstration et une version vierge. Ils ne sont pas publiés dans le dépôt.

### Contrôles statiques

- 5 feuilles dans chaque fichier : Guide, Mouvements, Stock, Tableau de bord et Listes.
- 406 cellules de formule par fichier.
- 7 règles de validation : référence de mouvement depuis la liste Stock ; type Entrée/Sortie ; motif ; catégorie ; quantité de mouvement > 0 ; stock initial >= 0 ; seuil >= 0.
- 2 plages d'AutoFiltre configurées : Mouvements A1:H501 et Stock A1:M101.
- Le calcul des lignes Stock vides renvoie désormais une cellule visuellement vide au lieu de zéro.
- Les dates de mouvements sont affichées au format ISO ; la colonne Date a été élargie.

### Résultats recalculés

| Scénario | Résultat vérifié |
|---|---|
| Démonstration initiale | GNT-001 = 8 ; CLN-002 = 24 ; JNT-003 = 3 |
| Tableau de bord initial | 3 références ; 2 alertes ; 0 stock négatif ; 1 OK ; 4 mouvements ; 35 unités |
| Seuil exact | Stock 3, seuil 3 : À COMMANDER |
| Stock négatif | Stock -1 : STOCK NÉGATIF ; compteur négatif = 1 |
| Frontière de capacité | Référence en ligne 101 et mouvement en ligne 501 : stock 15, référence comptée, mouvement compté |
| Version vierge | Tous les indicateurs à zéro |

### Mise en page

L'export PDF donne 5 pages pour la démonstration et 6 pages pour la version vierge. Les pages Guide et Tableau de bord tiennent sur une page ; Mouvements est en A4 paysage ; Stock est en A3 paysage avec en-tête répété ; Listes tient sur une page.

### Limites restantes

- Les règles et listes de validation sont configurées et leurs propriétés ont été relues, mais le clic utilisateur et les boîtes d'erreur n'ont pas encore été testés dans l'interface graphique.
- Les filtres sont configurés mais leur manipulation interactive reste à vérifier.
- Les références Stock en double ne sont pas encore bloquées automatiquement.
- Excel n'a pas été testé ; aucun test utilisateur externe n'a été réalisé.
- Le prototype n'est pas encore proposé à la livraison commerciale.

Le détail est consigné dans [le rapport de contrôle du 14 novembre](controle-prototype-suivi-stock-14-nov-2026.md).