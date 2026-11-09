# Audit du livrable de suivi de stock — 9 novembre 2026

## Objet

Vérifier le fichier réellement disponible dans l'espace de travail et le distinguer de la version ODS v2.1 décrite dans les documents du dépôt.

## Fichier inspecté

- Nom : `Tableaux_Methodes_Suivi_Stock_v1.ods`
- Taille : 32 910 octets
- Format : ODS (LibreOffice Calc)
- Fichier ouvert et inspecté directement dans son contenu ODS.

## Structure observée

| Feuille | Lignes observées | Formules |
|---|---:|---:|
| Guide | 11 | 0 |
| Mouvements | 5 (en-tête + 4 opérations fictives) | 0 |
| Stock | 4 (en-tête + 3 références fictives) | 6 |
| Tableau de bord | 8 | 5 |
| Listes | 8 | 0 |

Dans la feuille Stock, les colonnes « Entrées cumulées » et « Sorties cumulées » contiennent des valeurs saisies manuellement. Les seules formules de cette feuille calculent le stock actuel à partir de ces valeurs et déterminent l'alerte. Aucune formule ne relie la feuille Mouvements à la feuille Stock.

Le guide de la version 1 indique lui-même que les totaux d'entrées et de sorties doivent être renseignés manuellement et que le journal Mouvements sert à conserver le détail.

## Conclusion sur le fichier v1

La maquette v1 peut servir à illustrer une présentation de stock simple, mais elle ne réalise pas le calcul automatique depuis le journal des mouvements. Elle ne doit pas être vendue ou remise comme le modèle automatisé décrit sur le site.

Les calculs statiques visibles dans les trois exemples sont cohérents :
- Gants nitrile : 10 + 0 − 2 = 8 ; alerte À COMMANDER.
- Nettoyant : 20 + 10 − 6 = 24 ; alerte OK.
- Joint 20 mm : 5 + 0 − 2 = 3 ; alerte À COMMANDER.

Ces résultats ne valident pas une automatisation du journal des mouvements.

## Écart avec la documentation v2.1

Le dépôt contient un cahier des charges et un journal de tests qui décrivent un ODS v2.1 avec cinq feuilles, 405 formules, 100 références et 500 mouvements. Le journal rapporte des recalculs réussis dans LibreOffice Calc.

Cependant, le fichier v2.1 lui-même n'est pas publié dans le dépôt et n'était pas présent dans l'espace de travail inspecté lors de cet audit. Il n'a donc pas été possible de l'ouvrir, de confirmer son contenu, ni de le remettre avec ce compte rendu. Cela ne prouve pas qu'il n'existe pas ailleurs ; cela signifie seulement qu'il n'est pas vérifiable ou livrable depuis cet espace de travail.

## Actions requises avant livraison commerciale

1. Récupérer le véritable fichier v2.1 correspondant au journal de tests et le contrôler à nouveau, ou reconstruire le classeur si le fichier source est introuvable.
2. Vérifier les formules dans LibreOffice Calc sur une copie de test.
3. Contrôler visuellement les filtres.
4. Ajouter et tester les validations de saisie, notamment les types Entrée/Sortie et les quantités positives.
5. Détecter ou documenter les références inconnues et en double.
6. Créer une version vierge sans exemples fictifs et la faire tester par une personne non technique.
7. Ne remettre que le fichier effectivement contrôlé, avec sa version exacte.

## État commercial

Aucun e-mail commercial envoyé, aucune dépense engagée et aucun engagement juridique pris. Les prix affichés restent des tarifs de lancement soumis à confirmation du périmètre avant toute réalisation.
