# Contrôle du suivi de maintenance v1.1 — 20 novembre 2026

## Défaut constaté et corrigé

La démonstration v1.1 affichait dans la feuille Équipements une dernière préventive pour VAN-003 (10/11/2026), alors que le journal contenait une intervention de type Contrôle le 12/11/2026. La date calculée était donc vide et l'équipement apparaissait « À RENSEIGNER », en contradiction avec l'exemple public.

Correction appliquée à la démonstration : la ligne VAN-003 du journal est maintenant une maintenance préventive réalisée le 10/11/2026 (0,5 h). Le commentaire est fictif. Le tableau de bord affiche désormais VERSION 1.1 dans la démonstration et la version vierge.

## Vérifications effectuées dans LibreOffice Calc (UNO)

- VAN-003 : dernière préventive = 10/11/2026.
- VAN-003 : prochaine échéance = 08/02/2027 (périodicité 90 jours).
- VAN-003 : statut = À JOUR.
- Tableau de bord : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions, 5 heures.
- Test temporaire : ajout d'une préventive réalisée le 12/11/2026 pour POM-001 ; la dernière préventive passe au 12/11/2026.
- Test temporaire : ajout ensuite d'une corrective le 15/11/2026 ; la dernière préventive reste au 12/11/2026.
- Les tests temporaires ont été réalisés sur une copie et ne sont pas présents dans le fichier livré.

## Limites

Les tests sont des tests de calcul et de comportement via l'automatisation LibreOffice Calc UNO. Ils ne remplacent pas une recette visuelle au clavier et à la souris, un contrôle complet des validations, des filtres, du copier-coller, des impressions, de la compatibilité Excel ou un test utilisateur extérieur. Le classeur reste un prototype non disponible à la livraison et ne constitue pas une GMAO.
