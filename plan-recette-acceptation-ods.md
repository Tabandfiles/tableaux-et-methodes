# Plan de recette manuelle — prototypes ODS

**But :** compléter les contrôles structurels et les recalculs automatisés par des essais au clic dans LibreOffice Calc. Ce document est une grille de test, pas la preuve que les essais ont été réalisés.

## Préparation

- Travailler sur une copie de chaque fichier, jamais sur l'original de référence.
- Noter la version exacte de LibreOffice, le système utilisé et la date du test.
- Utiliser uniquement les données fictives fournies ; ne pas saisir de données personnelles ou confidentielles.
- Pour chaque essai, noter : résultat attendu, résultat observé, PASS/FAIL, commentaire et capture éventuelle.

## Tests communs aux trois produits

| ID | Manipulation | Résultat attendu |
|---|---|---|
| C-01 | Ouvrir le fichier, enregistrer sous un nouveau nom, fermer et rouvrir | Le classeur se rouvre sans avertissement de réparation ni perte de formule |
| C-02 | Cliquer sur chaque cellule avec liste de saisie | La liste attendue apparaît et une valeur autorisée peut être choisie |
| C-03 | Saisir une valeur interdite dans une cellule contrôlée | Le comportement de validation annoncé est observé ; noter si la saisie est bloquée ou seulement signalée |
| C-04 | Activer puis retirer chaque filtre | Les lignes sont filtrées sans décaler les données ni masquer les en-têtes |
| C-05 | Trier une colonne | Les données de chaque ligne restent solidaires |
| C-06 | Copier-coller une plage d'une ligne à l'autre | Les formules et validations restent cohérentes ; aucun écrasement involontaire |
| C-07 | Ajouter une ligne dans la dernière ligne prévue | Les formules et indicateurs couvrent bien la ligne limite |
| C-08 | Exporter en PDF depuis Calc | Les titres, en-têtes et colonnes utiles restent lisibles ; aucune colonne essentielle n'est coupée |

## Suivi de stock v2.2

| ID | Manipulation | Résultat attendu |
|---|---|---|
| S-01 | Choisir une référence de stock dans un mouvement | La liste propose les références renseignées dans Stock |
| S-02 | Saisir un type autre que Entrée ou Sortie | La validation signale ou bloque la valeur non autorisée selon le réglage configuré |
| S-03 | Saisir une quantité nulle ou négative | La validation doit refuser ou signaler la saisie ; confirmer le comportement réel |
| S-04 | Augmenter une sortie de GNT-001 | Le stock actuel et l'alerte se recalculent |
| S-05 | Amener le stock exactement au seuil | L'état devient À COMMANDER |
| S-06 | Créer volontairement une référence en double | Les lignes concernées affichent DOUBLON et le compteur augmente ; la saisie n'est pas censée être bloquée |
| S-07 | Filtrer Stock et Mouvements par référence et type | Les lignes attendues restent visibles et les calculs ne changent pas |
| S-08 | Atteindre la 100e référence et le 500e mouvement | Les cellules de calcul de la dernière ligne sont présentes |

## Registre d'interventions v1.0

| ID | Manipulation | Résultat attendu |
|---|---|---|
| I-01 | Choisir Type, Priorité et Statut | Les listes proposées correspondent à la feuille Listes |
| I-02 | Saisir une date hors plage ou du texte dans une date | La validation configurée réagit ; noter le comportement réel |
| I-03 | Saisir une durée négative | La validation doit refuser ou signaler la saisie ; confirmer le comportement réel |
| I-04 | Créer volontairement un identifiant en double | Les deux lignes sont signalées et le compteur indique deux lignes en doublon |
| I-05 | Marquer une intervention urgente comme En cours | Elle reste comptée parmi les urgences non terminées |
| I-06 | Marquer une urgence comme Terminée ou Annulée | Elle n'est plus comptée parmi les urgences non terminées |
| I-07 | Filtrer par statut, priorité, technicien et site | Le filtre restitue les lignes correspondantes |
| I-08 | Atteindre la 200e intervention | Les formules de contrôle et indicateurs couvrent la ligne 201 |

## Suivi de maintenance v1.0

| ID | Manipulation | Résultat attendu |
|---|---|---|
| M-01 | Saisir un équipement avec périodicité et dernière préventive | La prochaine échéance est calculée par addition des jours |
| M-02 | Modifier la dernière préventive | La prochaine échéance et le statut se recalculent |
| M-03 | Déplacer une échéance dans le passé | Le statut devient EN RETARD |
| M-04 | Déplacer une échéance dans les 30 jours | Le statut devient À PLANIFIER |
| M-05 | Déplacer une échéance au-delà de 30 jours | Le statut devient À JOUR |
| M-06 | Créer un identifiant d'équipement en double | Les lignes concernées affichent DOUBLON et le compteur augmente |
| M-07 | Ajouter une intervention préventive au journal sans modifier Équipements | La date de dernière préventive ne change pas automatiquement ; confirmer cette limite dans l'interface |
| M-08 | Filtrer équipements et interventions | Les filtres fonctionnent sans désolidariser les lignes |
| M-09 | Atteindre le 100e équipement et la 500e intervention | Les formules et indicateurs couvrent les lignes limites |

## Critères de sortie

Un produit ne pourra être déclaré prêt à la livraison qu'après :
1. réussite de tous les tests critiques ;
2. correction ou documentation des échecs non critiques ;
3. vérification du rendu écran et impression ;
4. test par une personne extérieure au projet ;
5. décision explicite sur la compatibilité Excel (ne pas l'annoncer sans essai dédié).

**État au 17/11/2026 :** cette recette manuelle n'a pas encore été exécutée. Les recalculs en mode sans interface et les contrôles structurels sont consignés dans [le rapport de contrôle du 17 novembre](controle-prototypes-17-nov-2026.md).
