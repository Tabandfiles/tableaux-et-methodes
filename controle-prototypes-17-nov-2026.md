# Contrôle du projet — 17 novembre 2026

## Résumé

Les trois familles de prototypes ODS ont été recalculées à nouveau avec LibreOffice Calc en mode sans interface, dans des copies de contrôle. Les guides ont été harmonisés avec les versions des fichiers. Aucun prototype n'est déclaré prêt à la vente.

## Dépôt GitHub

- Dépôt public : https://github.com/Tabandfiles/tableaux-et-methodes
- Branche par défaut : `main`.
- Commit observé au début du contrôle : `4c408c837795c6e767cd5f8da0321cb703227c91`.
- L'arborescence contenait 27 fichiers au début du contrôle ; aucun classeur ODS ou XLSX n'est publié dans le dépôt.
- Dernier workflow Pages observé : [43935743629](https://github.com/Tabandfiles/tableaux-et-methodes/actions/runs/43935743629), terminé avec succès le 16/11/2026 sur le commit `4c408c8`.

Les six classeurs demeurent des livrables de travail locaux et ne sont pas ajoutés au dépôt public.

## Audit des six classeurs locaux

Les six fichiers ont été ouverts puis réenregistrés par LibreOffice Calc en mode sans interface le 17/11/2026. Contrôles effectués après recalcul : noms des feuilles, nombre de cellules de formule, présence des règles de validation et filtres automatiques, absence de marqueurs d'erreur visibles dans le XML (`#NAME?`, `#VALUE!`, `#REF!`, `#DIV/0!`, `#N/A`, `#NUM!`) et intégrité ZIP/ODS.

| Produit | Feuilles | Formules par fichier | Règles de validation | Filtres | Capacité de conception |
|---|---:|---:|---:|---:|---|
| Stock v2.2 | 5 | 507 | 7 | 2 | 100 références / 500 mouvements |
| Registre d'interventions v1.0 | 4 | 210 | 5 | 1 | 200 interventions |
| Suivi de maintenance v1.0 | 5 | 408 | 9 | 2 | 100 équipements / 500 interventions |

Chaque produit existe en démonstration fictive et en version vierge. Les six versions vierges ont des indicateurs de tableau de bord à zéro après recalcul.

### Suivi de stock v2.2

Résultats de démonstration recalculés :
- GNT-001 : stock actuel 8.
- CLN-002 : stock actuel 24.
- JNT-003 : stock actuel 3.
- Tableau de bord : 3 références, 2 articles à commander, 0 stock négatif, 1 article au-dessus du seuil, 4 mouvements, 35 unités au total, 0 doublon.

Le guide des deux fichiers stock a été corrigé : le titre et le statut indiquent désormais v2.2, et non v2.1. Les références en double sont signalées, mais la saisie n'est pas bloquée.

### Registre d'interventions v1.0

Résultats de démonstration recalculés :
- 6 interventions, une dans chacun des six statuts.
- 1 intervention urgente non terminée.
- 0 doublon.
- 2 heures enregistrées.

Les doublons sont signalés, mais non bloqués.

### Suivi de maintenance v1.0

Résultats de démonstration recalculés :
- 3 équipements : 1 en retard, 1 à planifier sous 30 jours, 1 à jour.
- 4 interventions et 5 heures.
- 0 doublon et 0 fiche à compléter.

Limite fonctionnelle importante : la date de dernière maintenance préventive doit être mise à jour manuellement dans la feuille Équipements. Le journal Interventions ne synchronise pas cette date. Le classeur n'est pas une GMAO.

## Limites communes avant commercialisation

- Les clics réels dans l'interface graphique de Calc (listes, filtres, messages STOP et copier-coller) restent à tester.
- Aucun test utilisateur extérieur n'a été réalisé.
- Excel n'a pas été testé.
- Les doublons sont signalés, pas bloqués.
- Les capacités indiquées sont des plages prévues dans les formules et filtres, pas une garantie de performance sur tout poste.
- Les fichiers corrigés et recalculés du 17/11 sont regroupés dans l'archive locale `Tableaux_Methodes_Prototypes_17-11-2026.zip`, qui contient six ODS et une notice.

## Site public

Site relu le 17/11/2026 : https://tabandfiles.github.io/tableaux-et-methodes/

- Page accessible, en français, et service annoncé à distance partout en France.
- Métadonnées title, description, canonical et Open Graph présentes.
- Les offres sont des créations à la demande, pas des fichiers immédiatement téléchargeables.
- Le suivi de stock et le suivi de maintenance sont explicitement indiqués comme en préparation et non disponibles à la livraison.
- La carte du registre d'interventions a été modifiée : elle indique désormais explicitement « prototype en préparation, non disponible à la livraison », la capacité de conception de 200 interventions et les essais Calc encore requis.
- `robots.txt` et `sitemap.xml` sont accessibles. Le sitemap référence une seule page HTML : la page d'accueil.
- Aucune page de mentions légales ou de confidentialité n'est liée depuis la page publique ; les brouillons du dépôt restent incomplets faute d'informations réelles de l'exploitant.

## Prospection nationale

Audit du CSV avec un parseur respectant les champs entre guillemets :
- 27 entreprises distinctes.
- 17 colonnes pour chacune des 27 lignes.
- 18 territoires représentés : 13 régions métropolitaines et 5 DROM.
- 27 lignes avec une URL de source.
- 16 e-mails publics et 25 téléphones publics recensés.
- 0 doublon.
- 0 besoin marqué confirmé.
- 0 contact marqué effectué.
- Dates de recherche présentes : du 05/11/2026 au 17/11/2026.
- Trois coordonnées ont été revalidées le 17/11 sur des sites officiels : ASI BAT (Île-de-France), ETS Jumelle (Hauts-de-France) et DEMS (Centre-Val de Loire). Les détails et réserves sont consignés dans `premiers-prospects.md`.

Ce contrôle est structurel : il ne revalide pas chaque coordonnée individuellement. Seules les trois fiches ci-dessus ont été relues sur leurs sites officiels le 17/11. Avant toute démarche, vérifier à nouveau la page officielle, le rôle du destinataire, le canal approprié et toute opposition. Ne pas utiliser les coordonnées d'urgence ou de dépannage comme canal commercial.

## Garde-fous

Aucun e-mail commercial, appel ou formulaire n'a été envoyé ou soumis. Aucune dépense n'a été engagée et aucun engagement juridique n'a été pris.
