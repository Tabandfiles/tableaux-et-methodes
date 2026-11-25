# Contrôle du Tableau simple v1.1 — 25 novembre 2026

## Périmètre

Contrôle des deux fichiers ODS issus du pack local du 24/11/2026, sur copies de travail, avec LibreOffice Calc 25.2.3.2 en mode sans interface graphique (UNO) et inspection des exports PDF.

## Défaut découvert

La version vierge contenait 50 lignes de saisie prévues, mais sa zone d'impression de la feuille `Suivi` s'arrêtait à la ligne 24 (plage A1:I24). L'export PDF ne montrait donc que 20 lignes vierges au lieu des 50 prévues.

## Correction appliquée

- Version de travail portée à v1.1.
- Zone d'impression de `Suivi` étendue à A1:I54 (en-tête et 50 lignes de saisie).
- Démonstration conservée sans changement fonctionnel ; ses six demandes fictives restent visibles.
- Les deux fichiers ont été exportés à nouveau en PDF depuis LibreOffice Calc.

## Vérifications effectuées

| Contrôle | Démonstration | Version vierge |
|---|---:|---:|
| Ouverture Calc | OK | OK |
| Feuilles | 3 | 3 |
| Lignes de saisie prévues | 50 | 50 |
| Demandes fictives | 6 | 0 |
| Règles de validation | 2 | 2 |
| Cellules portant une validation | 100 | 100 |
| Plage de filtre déclarée | 1 | 1 |
| Formules | 0 | 0 |
| Erreurs de formule après recalcul | 0 | 0 |
| Export PDF | 2 pages | 3 pages |

La zone d'impression de la version vierge a été relue après sauvegarde : A1:I54. Les pages 2 et 3 du PDF vierge ont été inspectées : elles présentent chacune 25 lignes vierges, soit les 50 lignes prévues. La page 2 du PDF de démonstration montre les six demandes fictives.

## Ce qui n'est PAS validé

- ouverture et choix dans les listes déroulantes à la souris ;
- blocage effectif d'une valeur interdite via l'interface ;
- manipulation réelle des filtres et du tri ;
- copier-coller manuel dans Calc ;
- test utilisateur extérieur ;
- compatibilité Microsoft Excel ;
- impression physique.

## Conclusion

Le défaut de plage d'impression de la version vierge est corrigé et vérifié dans le PDF. Le classeur reste un prototype en attente de recette interactive et de test extérieur ; il n'est pas déclaré prêt à la livraison comme modèle standard.
