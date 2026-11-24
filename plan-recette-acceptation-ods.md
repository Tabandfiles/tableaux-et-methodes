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


## Tableau simple — suivi de demandes (plan ajouté le 24/11/2026)

Ce plan complète la recette des trois prototypes automatisés. Il décrit les essais à effectuer sur une copie de la démonstration et sur une copie vierge. **Les tests ci-dessous ne sont pas déclarés exécutés.**

| ID | Manipulation | Résultat attendu |
|---|---|---|
| TS-01 | Ouvrir le fichier ODS, l'enregistrer sous un nouveau nom, fermer puis rouvrir | Le classeur s'ouvre sans réparation ni perte de mise en page |
| TS-02 | Cliquer sur une cellule Priorité | La liste propose uniquement les valeurs documentées dans le guide |
| TS-03 | Cliquer sur une cellule Statut | La liste propose uniquement les statuts documentés dans le guide |
| TS-04 | Saisir une valeur hors liste dans Priorité et Statut | Le comportement réel de validation est constaté et noté ; ne pas annoncer un blocage si la saisie est seulement signalée |
| TS-05 | Activer un filtre sur Statut puis sur Priorité | Les lignes attendues sont affichées sans désolidariser les données |
| TS-06 | Trier par date cible ou priorité | Les informations de chaque demande restent sur la même ligne |
| TS-07 | Copier-coller une ligne existante dans une autre ligne prévue | Les validations, formats et éventuelles formules restent cohérents |
| TS-08 | Compléter la dernière ligne prévue (50e demande) | Les validations et le format restent présents jusqu'à la dernière ligne |
| TS-09 | Ouvrir la version vierge | Aucune donnée de démonstration ne subsiste ; le guide et les listes sont présents |
| TS-10 | Exporter la démonstration et la version vierge en PDF | Les titres et colonnes utiles restent lisibles, sans page blanche ni colonne essentielle coupée |

### Critères de sortie propres au Tableau simple

- Tous les tests critiques TS-01 à TS-09 réussissent dans LibreOffice Calc.
- Les éventuels échecs sont corrigés ou explicitement documentés.
- Le PDF est relu visuellement après export depuis Calc.
- Une personne extérieure au projet réalise un scénario d'utilisation simple.
- La version et le système de LibreOffice sont consignés.
- Excel reste non certifié tant qu'un essai dédié n'a pas été effectué.

**Contrôle partiel du 24/11/2026 :** les deux ODS (démonstration et version vierge) ont été ouverts, enregistrés sous une copie puis rouverts avec LibreOffice Calc 25.2.3.2 via UNO. Les trois feuilles sont présentes ; la capacité de 50 lignes est conservée ; les validations de liste Priorité (`Priorites`) et Statut (`Statuts`) sont présentes en première et dernière ligne et persistent après réouverture ; une copie temporaire conserve la validation ; les PDF exportés depuis Calc ont été inspectés (2 pages pour la démonstration, 3 pour la version vierge). Le XML déclare une plage de filtre `Suivi.A4:I54` avec boutons, mais les menus de filtre n'ont pas été manipulés au clic. Les saisies interdites, le tri, le copier-coller manuel, le test extérieur, Excel et l'impression physique restent à faire. Le produit n'est pas déclaré prêt à la vente. Voir `controle-tableau-simple-24-nov-2026.md`.