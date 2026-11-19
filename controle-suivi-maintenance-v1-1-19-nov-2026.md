# Contrôle ciblé — suivi de maintenance v1.1 (19 novembre 2026)

## Changement du prototype

La feuille `Equipements`, colonne `Dernière préventive` (G2:G101), calcule automatiquement la date la plus récente du journal `Interventions` pour le même identifiant, lorsque le type est `Préventive` et le résultat `Réalisée`.

La prochaine échéance reste calculée par `Dernière préventive + périodicité`. Les interventions correctives et les préventives non réalisées ne repoussent pas l'échéance.

## Vérifications réalisées avec LibreOffice Calc via UNO

| Test | Résultat observé |
|---|---|
| Démonstration initiale POM-001 | Dernière préventive 01/11/2026 ; prochaine échéance 01/12/2026 |
| Ajout d'une préventive réalisée au 12/11/2026 | Dernière préventive 12/11/2026 ; prochaine échéance 12/12/2026 |
| Ajout d'une corrective réalisée au 15/11/2026 | La date préventive reste au 12/11/2026 |
| Ajout d'une préventive « À planifier » au 18/11/2026 | La date préventive reste au 12/11/2026 |
| Détection d'un ID équipement en double | Les deux lignes affichent `DOUBLON` |
| Version vierge, nouvel équipement et préventive réalisée au 10/11/2026 | Dernière préventive 10/11/2026 ; échéance 25/12/2026 pour une périodicité de 45 jours |
| Tableau de bord vierge après saisie de test | 1 équipement renseigné |
| Filtres automatiques | 101 lignes pour Équipements ; 501 lignes pour Interventions |
| Structure des deux fichiers | 5 feuilles et 508 formules par fichier |
| Archive ODS | ZIP valide, aucun marqueur d'erreur de formule visible détecté dans le XML |

Les saisies de test ont été réalisées dans des copies temporaires ; les fichiers livrés ne contiennent pas les données de test ajoutées.

## Limites restantes

- Les clics visuels et le comportement des messages de validation dans l'interface graphique ne sont pas certifiés par ce test UNO.
- L'impression et la compatibilité Excel ne sont pas testées.
- Le classeur n'est pas une GMAO et ne gère pas les pièces, contrats, notifications ni conformité réglementaire.
- Les doublons sont signalés mais pas bloqués.

**Statut : prototype amélioré, toujours en préparation et non disponible à la livraison.**
