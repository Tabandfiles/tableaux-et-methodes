# Contrôle du prototype de suivi de stock ODS v2.1 — 14 novembre 2026

## Fichiers de travail créés

- Démonstration : Tableaux_Methodes_Suivi_Stock_demo_v2_1.ods (50 849 octets au contrôle final).
- Version vierge : Tableaux_Methodes_Suivi_Stock_vierge_v2_1.ods (50 279 octets au contrôle final).
- Les deux fichiers sont présents dans l'espace de travail local. Ils ne sont pas publiés dans GitHub afin de ne pas rendre le modèle commercial complet librement téléchargeable.

## Structure et configuration

Chaque fichier contient cinq feuilles : Guide, Mouvements, Stock, Tableau de bord et Listes, ainsi que 406 cellules de formule.

Capacité de conception : 100 références (Stock lignes 2 à 101) et 500 mouvements (Mouvements lignes 2 à 501).

Validations configurées :

- Mouvements B2:B501 : référence choisie dans la liste des références Stock.
- Mouvements D2:D501 : liste Entrée / Sortie.
- Mouvements E2:E501 : nombre strictement supérieur à zéro.
- Mouvements F2:F501 : liste de motifs.
- Stock C2:C101 : liste de catégories.
- Stock F2:F101 : stock initial positif ou nul.
- Stock J2:J101 : seuil positif ou nul.

Deux AutoFiltres sont configurés : Mouvements A1:H501 et Stock A1:M101. Les lignes Stock sans référence restent visuellement vides au lieu d'afficher des zéros. La colonne Date des mouvements a été élargie et utilise un affichage ISO. La colonne MAJ a été renommée Date inventaire, saisie manuellement.

## Tests de calcul recalculés avec LibreOffice Calc

| Test | Résultat |
|---|---|
| Démonstration initiale | GNT-001 = 8 ; CLN-002 = 24 ; JNT-003 = 3 |
| Tableau de bord initial | 3 références ; 2 alertes ; 0 négatif ; 1 OK ; 4 mouvements ; 35 unités |
| Seuil exact | Ajout d'une sortie de 5 et seuil réglé à 3 : stock 3, alerte À COMMANDER |
| Stock négatif | Ajout d'une sortie de 9 : stock -1, alerte STOCK NÉGATIF, compteur négatif = 1 |
| Frontière de capacité | Référence ajoutée en ligne 101 et mouvement en ligne 501 : stock calculé à 15, 4 références et 5 mouvements comptés |
| Version vierge | Tous les indicateurs du tableau de bord à zéro |

Les formules de stock et d'alerte ont été recalculées après chaque scénario. Le nombre de formules reste 406 dans les deux fichiers.

## Contrôle de mise en page

Export PDF réalisé depuis LibreOffice : 5 pages pour la démonstration et 6 pages pour la version vierge. Le Guide et le tableau de bord tiennent sur une page chacun ; Mouvements est en A4 paysage ; Stock est en A3 paysage avec en-tête répété ; Listes tient sur une page. La démonstration n'a plus de page de débordement vide.

## Limites et décision commerciale

- Les règles de validation sont configurées et leurs propriétés ont été relues, mais le choix réel dans les listes déroulantes et les messages de refus doivent encore être testés par interaction dans l'interface graphique.
- Les filtres sont configurés, mais leur manipulation interactive reste à vérifier.
- Les références en double ne sont pas encore bloquées automatiquement ; la règle d'unicité est donc encore à contrôler manuellement.
- Les tests ont été réalisés avec LibreOffice en mode sans interface et par export PDF. Excel n'a pas été testé.
- Aucun utilisateur externe n'a encore essayé le fichier.

Conclusion : le prototype v2.1 est fonctionnel sur les scénarios de calcul testés, mais il n'est pas encore disponible à la livraison commerciale. Le statut public du suivi de stock reste donc « en préparation » jusqu'au contrôle interactif et au test utilisateur.