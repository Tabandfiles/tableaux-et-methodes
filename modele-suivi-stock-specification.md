# Cahier des charges — Suivi de stock

**Produit :** Suivi de stock simple  
**Prix de lancement affiché :** 20 € pour le périmètre de base  
**Format :** LibreOffice Calc (.ods)  
**Version de travail :** 2.1 — 9 novembre 2026

## Statut réel

Le journal de travail daté du 9 novembre rapporte qu'un modèle ODS v2.1 a été créé et recalculé avec LibreOffice Calc. Il décrit cinq feuilles : Guide, Mouvements, Stock, Tableau de bord et Listes, avec une cible de 100 références et 500 mouvements et 405 cellules de formule. **Contrôle de disponibilité du 12 novembre : le binaire ODS n'est pas présent dans le dépôt public ni dans les fichiers accessibles pour cette vérification ; ces résultats historiques ne peuvent pas être rejoués aujourd'hui.**

Les mouvements alimentent automatiquement les cumuls par référence. Le stock actuel est calculé à partir du stock initial, des entrées et des sorties. L'alerte distingue trois états : STOCK NÉGATIF, À COMMANDER et OK.

Le fichier de travail doit être remis séparément ; il n'est pas publié dans le dépôt public afin de ne pas mettre gratuitement à disposition le modèle commercial complet. Tant que le binaire n'est pas récupéré ou reconstruit et recontrôlé, aucun fichier automatisé ne doit être présenté comme disponible à la livraison. Excel n'a pas été testé.

## Structure du classeur

### Feuille « Stock »

| Colonne | Nom | Utilisation |
|---|---|---|
| A | Référence | Identifiant unique à respecter |
| B | Article | Nom de l'article |
| C | Catégorie | Famille d'articles |
| D | Emplacement | Réserve, atelier, véhicule, etc. |
| E | Fournisseur | Fournisseur habituel, facultatif |
| F | Stock initial | Quantité au démarrage |
| G | Entrées cumulées | Calcul automatique depuis Mouvements |
| H | Sorties cumulées | Calcul automatique depuis Mouvements |
| I | Stock actuel | Stock initial + entrées − sorties |
| J | Seuil d'alerte | Niveau minimal choisi |
| K | Alerte | STOCK NÉGATIF / À COMMANDER / OK |
| L | Dernière mise à jour | Date de contrôle manuel |
| M | Commentaires | Informations facultatives |

### Feuille « Mouvements »

Une ligne par opération : Date, Référence, Article, Type, Quantité, Motif, Personne / service et Commentaire. La quantité doit être positive ; le type doit être exactement Entrée ou Sortie.

### Autres feuilles

- **Guide :** mode d'emploi et limites du modèle.
- **Tableau de bord :** références renseignées, articles à commander, articles au-dessus du seuil, mouvements enregistrés et quantité totale en stock.
- **Listes :** valeurs de référence pour les catégories, types et motifs. Cette feuille n'alimente pas encore de menus déroulants.

## Logique de calcul

- Entrées cumulées : somme des quantités des mouvements de type Entrée pour la référence.
- Sorties cumulées : somme des quantités des mouvements de type Sortie pour la référence.
- Stock actuel : stock initial + entrées cumulées − sorties cumulées.
- Alerte : si le stock est négatif, afficher STOCK NÉGATIF ; sinon, si le stock est inférieur ou égal au seuil, afficher À COMMANDER ; sinon afficher OK.

Selon le contrôle consigné le 9 novembre, les formules étaient présentes dans le fichier ODS de travail et recalculées dans LibreOffice Calc. Le binaire étant indisponible lors du contrôle du 12 novembre, ce résultat historique ne peut pas être reproduit ici. Les références inconnues ne sont pas automatiquement ajoutées à la feuille Stock : elles doivent être rapprochées manuellement.

## Tests effectués le 9 novembre 2026

| Cas | Résultat attendu et observé | État |
|---|---|---|
| Gants : stock initial 10, sortie 2, seuil 10 | Stock 8 ; À COMMANDER | Réussi |
| Nettoyant : stock initial 20, entrée 10, sortie 6, seuil 8 | Stock 24 ; OK | Réussi |
| Joint : stock initial 5, sortie 2, seuil 5 | Stock 3 ; À COMMANDER | Réussi |
| Tableau de bord | 3 références, 2 alertes, 1 article OK, 4 mouvements, 35 unités | Réussi |
| Modification d'une sortie de 2 à 7 | Stock recalculé à 3 ; À COMMANDER | Réussi |
| Stock exactement égal au seuil | À COMMANDER | Réussi |
| Stock négatif | STOCK NÉGATIF | Réussi |
| Lignes de saisie inutilisées | Non comptées dans les indicateurs | Réussi |

Le journal détaillé est dans [tests-suivi-stock-v2-1.md](tests-suivi-stock-v2-1.md).

## Limites connues avant commercialisation

- Les listes de la feuille Listes ne sont pas encore reliées à des validations de données / menus déroulants.
- Les plages de filtres sont définies dans le fichier ; leur rendu doit encore être contrôlé visuellement à l'ouverture dans Calc.
- Les quantités négatives ne sont pas bloquées par une validation de saisie ; elles sont à éviter. Le stock négatif calculé est signalé.
- Pas de détection automatique des références en double ou inconnues.
- Pas de gestion des commandes fournisseurs, réservations, lots, numéros de série, inventaires multi-sites ou notifications.
- Les formules et l'ergonomie doivent être testées dans une session utilisateur réelle avant diffusion à grande échelle.
- La compatibilité Excel n'est pas testée et ne doit pas être promise.

## Périmètre de l'offre de base

Le tarif de lancement de 20 € correspond au modèle simple dans la limite de 100 références et 500 mouvements, avec une notice courte. Toute demande dépassant ce périmètre ou ajoutant des fonctions spécifiques doit être chiffrée avant réalisation. Le périmètre et le prix sont confirmés avant de commencer.

## Prochaines améliorations

1. Vérifier visuellement les filtres dans LibreOffice Calc.
2. Ajouter et tester les validations de données pour Type et Quantité.
3. Créer une copie vierge sans exemples fictifs pour la livraison client.
4. Tester avec une personne non technique et noter ses difficultés.
5. Tester séparément la compatibilité Excel si elle devient une demande commerciale.
