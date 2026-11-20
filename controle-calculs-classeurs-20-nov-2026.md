# Contrôle de calcul des trois prototypes — 20 novembre 2026

## Environnement

Tests réalisés avec LibreOffice Calc 25.2.3.2 via UNO. Les saisies supplémentaires ont été faites sur des copies temporaires des classeurs de démonstration ; les tests temporaires ont été abandonnés après vérification et ne figurent pas dans les fichiers livrés.

## Suivi de stock v2.2

État de départ fictif pour GNT-001 : stock actuel 8 ; le journal contient 4 mouvements ; total des stocks 35 unités.

Test : ajout temporaire d'une sortie de 1 unité pour GNT-001.

Résultats recalculés :
- GNT-001 : 7 unités.
- Mouvements enregistrés : 5.
- Quantité totale en stock : 34 unités.

Résultat : les calculs de stock et les indicateurs du tableau de bord se mettent à jour après l'ajout du mouvement.

## Registre d'interventions v1.0

État de départ fictif : 6 interventions, une dans chacun des six statuts.

Test : ajout temporaire d'une intervention INT-0007 de priorité normale et de statut « En cours ».

Résultats recalculés :
- Interventions enregistrées : 7.
- Interventions « En cours » : 2.

Résultat : le compteur global et le compteur du statut se mettent à jour.

## Suivi de maintenance v1.1

Une incohérence de démonstration a été corrigée : l'intervention VAN-003 correspond maintenant à une maintenance préventive réalisée le 10/11/2026, ce qui alimente la dernière préventive et l'échéance affichées.

Résultats recalculés :
- VAN-003 : dernière préventive 10/11/2026.
- VAN-003 : prochaine échéance 08/02/2027.
- VAN-003 : statut « À JOUR ».
- Tableau de bord : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions et 5 heures.

Test temporaire complémentaire sur POM-001 :
- Ajout d'une préventive réalisée le 12/11/2026 : la date de dernière préventive passe au 12/11/2026.
- Ajout ensuite d'une corrective le 15/11/2026 : la date de dernière préventive reste au 12/11/2026.

Résultat : la date calculée tient compte de la préventive réalisée la plus récente et n'est pas repoussée par une corrective ultérieure.

## Limites

Ces tests confirment des calculs et mises à jour de cellules via LibreOffice Calc UNO. Ils ne remplacent pas une recette visuelle au clavier et à la souris, un contrôle exhaustif des validations, filtres et copier-coller, les impressions, la compatibilité Excel ou un test utilisateur extérieur.

Les trois familles restent des prototypes non disponibles à la livraison. Les exemples sont fictifs. Aucun e-mail commercial, appel ou formulaire n'a été envoyé ; aucune dépense ni engagement juridique.
