# Fiche produit — Suivi de stock simple

**Tableaux & Méthodes — prix de lancement affiché : 20 €**  
**Format :** LibreOffice Calc (.ods)  
**Capacité cible de conception :** 100 références et 500 mouvements. Cette capacité n'est pas disponible à la livraison tant que le binaire final n'a pas été récupéré ou reconstruit et revalidé.

## Ce que comprend le modèle

- Une feuille Stock pour les articles, catégories, emplacements, fournisseurs, stocks initiaux et seuils.
- Un journal Mouvements pour enregistrer chaque entrée ou sortie.
- Le calcul automatique des entrées et sorties cumulées par référence.
- Le calcul du stock actuel.
- Trois états d'alerte : STOCK NÉGATIF, À COMMANDER et OK.
- Un tableau de bord récapitulatif.
- Un guide d'utilisation et une feuille de listes de référence.
- Des exemples entièrement fictifs.

## Ce qui n'est pas inclus dans le prix de base

Commandes fournisseurs, réservations, lots, numéros de série, multi-sites, notifications, imports complexes, macros et automatisations externes. Les menus déroulants de saisie ne sont pas encore configurés. Ces besoins doivent être évalués et chiffrés séparément avant tout engagement.

## Compatibilité

Le journal de tests daté du 9 novembre rapporte un recalcul de la version 2.1 avec LibreOffice Calc. Toutefois, le binaire ODS n'a pas été retrouvé dans le dépôt ni dans les fichiers accessibles le 12 novembre : les tests ne peuvent pas être rejoués aujourd'hui et aucun classeur automatisé n'est disponible à la livraison. Excel n'a pas été testé.

## Livraison et cadrage

Le besoin, le volume, le logiciel utilisé et les éventuelles adaptations sont confirmés avant réalisation. Le prix de lancement de 20 € concerne le périmètre simple décrit ci-dessus ; toute évolution supplémentaire fait l'objet d'un accord préalable.

## Statut

Le journal de tests conserve un compte rendu historique de la version de travail ODS v2.1. Le binaire v2.1 n'est pas disponible dans le dépôt ni dans les fichiers accessibles le 12 novembre ; il faut le récupérer ou reconstruire le classeur avant toute livraison. Après cela, il restera à vérifier visuellement les filtres, à ajouter des validations de saisie et à faire tester l'ergonomie par une personne non technique. Attention : le fichier v1 joint dans la conversation est une ancienne maquette à cumuls manuels, et non la v2.1. Ne pas remettre la v1 comme produit automatisé. Voir [l'audit du livrable](controle-livrable-suivi-stock-9-nov-2026.md).


## Mise à jour — 13 novembre 2026 : prototype v2.0

Un nouveau prototype ODS v2.0 a été reconstruit localement et recalculé avec LibreOffice Calc. Il comprend cinq feuilles, 406 cellules de formule, 100 lignes de références et 500 lignes de mouvements. Les exemples fictifs et les cas dynamiques (sortie augmentée, seuil exact, stock négatif) ont été rejoués ; la version vierge renvoie des indicateurs à zéro. Les deux fichiers de travail sont joints à la conversation, pas publiés dans le dépôt.

**Le prototype n'est pas encore prêt à la livraison commerciale.** Les menus déroulants et validations de saisie restent à configurer ; les filtres ne sont pas préconfigurés ; les références en double ou inconnues ne sont pas signalées ; les quantités négatives ne sont pas bloquées. L'interface Calc avec utilisateur, l'impression A4 et la compatibilité Excel ne sont pas validées. Une prévisualisation PDF a notamment montré une date trop étroite à l'impression. Conserver le statut « en préparation » sur le site jusqu'à correction et contrôle manuel.
