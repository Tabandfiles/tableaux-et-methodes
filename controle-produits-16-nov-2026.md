# Contrôle des prototypes, du site et de la prospection — 16 novembre 2026

## Dépôt et site public

- Dépôt public : [Tabandfiles/tableaux-et-methodes](https://github.com/Tabandfiles/tableaux-et-methodes), branche `main`, droits de lecture et de modification confirmés.
- Dernier commit observé avant cette mise à jour : `70a72e8` (15/11/2026).
- Site public relu le 16/11/2026 : [Tableaux & Méthodes](https://tabandfiles.github.io/tableaux-et-methodes/). La page est accessible et présente les offres à distance partout en France.
- Le sitemap ne référence que la page d'accueil, seule page HTML publique. `robots.txt` pointe vers ce sitemap.
- Les mentions légales et la politique de confidentialité ne sont pas publiées : les informations réelles de l'exploitant restent à fournir et à vérifier.

## Audit des six fichiers ODS locaux

Les six fichiers ont été contrôlés dans l'archive ODS et recalculés avec LibreOffice via UNO. Aucun texte d'erreur de formule visible (`#NAME?`, `#VALUE!`, `#REF!`, `#DIV/0!`, `#N/A`) n'a été détecté. Les filtres et validations sont présents. Les binaires ne sont pas publiés dans le dépôt.

| Produit | Feuilles | Formules par fichier | Règles de validation | Capacité de conception |
|---|---:|---:|---:|---|
| Stock v2.2 — démonstration et vierge | 5 | 507 | 7 | 100 références / 500 mouvements |
| Interventions v1.0 — démonstration et vierge | 4 | 210 | 5 | 200 interventions |
| Maintenance v1.0 — démonstration et vierge | 5 | 408 | 9 | 100 équipements / 500 interventions |

### Suivi de stock v2.2

- Filtres : Mouvements A1:H501 et Stock A1:N101.
- Démonstration : 3 références, 2 articles à commander, 0 stock négatif, 1 article OK, 4 mouvements, 35 unités, 0 doublon.
- Version vierge : indicateurs à zéro.
- Les références en double sont signalées, mais la saisie n'est pas bloquée.

### Registre d'interventions v1.0

- Filtre : Interventions A1:R201.
- Démonstration : 6 interventions, une dans chacun des six statuts, 1 urgente non terminée, 0 doublon et 2 heures.
- Version vierge : indicateurs à zéro.
- Les identifiants en double sont signalés, mais la saisie n'est pas bloquée.

### Suivi de maintenance v1.0

- Filtres : Equipements A1:M101 et Interventions A1:H501.
- Démonstration : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions, 5 heures, 0 doublon et 0 fiche à compléter.
- Version vierge : les huit indicateurs du tableau de bord sont à zéro.
- Exemple : Pompe P01, échéance 01/12/2026 ; CTA 02, échéance 31/10/2026 (en retard) ; Vanne V08, échéance 08/02/2027 (à jour).
- Test dynamique : la date de dernière préventive de CTA 02, déplacée au 16/11/2026, fait passer l'échéance au 16/12/2026 et le statut à À PLANIFIER.
- Test de doublon : deux lignes avec le même ID affichent DOUBLON ; compteur = 2.
- Test des limites : la 100e fiche équipement et la 500e intervention sont incluses dans les calculs et les indicateurs.
- **Limite centrale :** la date de dernière préventive est saisie et actualisée manuellement dans Equipements. Le journal Interventions ne synchronise pas cette date. Le classeur n'est pas une GMAO.

## Limites communes avant commercialisation

- Les clics réels dans l'interface graphique de LibreOffice Calc (listes, filtres, messages STOP et copier-coller) restent à tester.
- Aucun test utilisateur extérieur n'a été réalisé.
- Excel n'a pas été testé.
- Les doublons sont signalés, pas bloqués.
- Les prototypes restent des fichiers de travail locaux et ne sont pas disponibles au téléchargement sur le site.

## Prospection nationale

Le CSV a été relu structurellement le 16/11/2026 : 27 entreprises distinctes, 17 colonnes, 18 territoires (13 régions métropolitaines et 5 DROM), une URL source par ligne, aucune ligne mal formée, aucun contact marqué comme effectué et aucun besoin marqué comme confirmé.

Ce contrôle ne revalide pas chaque coordonnée individuelle. Les dates et sources de vérification sont conservées dans `premiers-prospects.md` et `suivi-prospection.csv` ; revérifier la page officielle, le destinataire, le canal et toute opposition avant un éventuel contact.

## Garde-fous

Aucun e-mail commercial, appel ou formulaire n'a été envoyé ou soumis. Aucune dépense n'a été engagée et aucun engagement juridique n'a été pris.
