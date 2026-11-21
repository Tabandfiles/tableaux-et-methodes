# Contrôle des zones d’impression des classeurs — 21 novembre 2026

## Périmètre

Six classeurs ODS : démonstration et version vierge du suivi de stock v2.2, du registre d’interventions v1.0 et du suivi de maintenance v1.1.

## Défauts observés avant correction

Les exports PDF du 20/11/2026 donnaient :
- Stock : 6 pages par classeur, avec des zones couvrant jusqu’à 500 mouvements et 100 références.
- Maintenance : 13 pages par classeur, avec 500 lignes d’interventions et 100 équipements imprimés même lorsque les lignes étaient vides.
- Registre : 4 pages ; le journal comportait 18 colonnes sur une seule page très large.
- Les descriptions longues du guide et le rappel du tableau de bord Maintenance étaient coupés à l’impression. Le rappel indiquait encore à tort que la dernière préventive devait être actualisée manuellement.

## Corrections réversibles

- Démonstrations : zones d’impression limitées aux en-têtes et données utiles.
- Versions vierges : première zone imprimable limitée à 30 lignes de mouvements/interventions et 20 références/équipements ; elle peut être étendue.
- Stock : la vue imprimée conserve les colonnes principales jusqu’à « Alerte » ; date d’inventaire, commentaires et contrôle de référence restent dans le classeur mais hors de cette vue.
- Maintenance : la vue imprimée des équipements conserve les colonnes principales jusqu’à « Statut » ; contrôle ID, responsable et commentaires restent dans le classeur mais hors de cette vue.
- Registre : impression du journal en deux panneaux (A:J puis K:R).
- Renvoi à la ligne dans les guides et notes des tableaux de bord ; hauteur des lignes optimisée et marges réduites.
- Maintenance : titre du guide harmonisé ; rappel du tableau de bord corrigé pour indiquer que la dernière préventive est calculée depuis le journal.

## Vérifications

- Six ODS réouverts et enregistrés avec LibreOffice Calc.
- Six exports PDF produits ; exactement 5 pages non vides par fichier.
- Pages Guide et Tableau de bord Maintenance inspectées visuellement en haute résolution : texte complet et rappel lisible.
- Page Équipements Maintenance inspectée : dix colonnes principales lisibles.
- Intégrité ZIP des six ODS vérifiée.
- Aucun marqueur d’erreur de formule visible (#NAME?, #VALUE!, #REF!, #DIV/0!, #N/A, #NUM!) dans le XML des six classeurs.

## Limites restantes

- L’export PDF ne remplace pas un essai sur imprimante physique.
- Les clics réels dans Calc, les messages de validation, le copier-coller et un test utilisateur extérieur restent à réaliser.
- Excel n’a pas été testé.
- Les doublons sont signalés mais pas bloqués.
- Aucun prototype n’est déclaré prêt à la vente.

Les données de démonstration sont fictives. Les six ODS et leurs six aperçus PDF sont regroupés dans le pack de travail du 21/11/2026.
