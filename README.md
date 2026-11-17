# Tableaux & Méthodes

Création à distance de tableaux de suivi sur mesure pour artisans, petites entreprises, associations et équipes de maintenance, partout en France. Les modèles sont conçus en priorité pour LibreOffice Calc.

- **Site public :** https://tabandfiles.github.io/tableaux-et-methodes/
- **Contact :** tabsandmethod@gmail.com
- **Dépôt :** https://github.com/Tabandfiles/tableaux-et-methodes

## État du projet au 17 novembre 2026

Trois familles de prototypes ODS existent en démonstration fictive et en version vierge. Les six fichiers de travail sont conservés hors du dépôt public et regroupés dans l'archive locale `Tableaux_Methodes_Prototypes_17-11-2026.zip`.

| Produit | Version | Feuilles | Formules par fichier | Validations | Filtres | Capacité de conception |
|---|---:|---:|---:|---:|---:|---|
| Suivi de stock | v2.2 | 5 | 507 | 7 | 2 | 100 références / 500 mouvements |
| Registre d'interventions | v1.0 | 4 | 210 | 5 | 1 | 200 interventions |
| Suivi de maintenance | v1.0 | 5 | 408 | 9 | 2 | 100 équipements / 500 interventions |

Le 17/11/2026, les six classeurs ont été ouverts puis réenregistrés avec LibreOffice Calc en mode sans interface. Les feuilles, cellules de formule, règles de validation et filtres ont été contrôlés ; aucun marqueur d'erreur de formule visible n'a été détecté dans le XML. Les versions vierges affichent zéro sur leurs indicateurs après recalcul.

**Aucun de ces prototypes n'est déclaré prêt à la vente.** Les clics réels dans l'interface graphique de Calc, les messages de validation, le copier-coller, l'impression et un test utilisateur extérieur restent à vérifier. Excel n'a pas été testé. Les doublons sont signalés mais non bloqués.

Voir le [rapport de contrôle du 17 novembre](controle-prototypes-17-nov-2026.md) et le [plan de recette manuelle](plan-recette-acceptation-ods.md).

## Résumé des produits

### Suivi de stock v2.2
- Feuilles : Guide, Mouvements, Stock, Tableau de bord, Listes.
- Stock actuel calculé à partir du stock initial et du journal Entrées/Sorties.
- Alertes : stock négatif, à commander, OK.
- Références en double signalées, sans blocage.
- Démonstration recalculée : GNT-001 = 8, CLN-002 = 24, JNT-003 = 3 ; 3 références, 2 alertes, 0 stock négatif, 1 OK, 4 mouvements, 35 unités et 0 doublon.

### Registre d'interventions v1.0
- Feuilles : Guide, Interventions, Tableau de bord, Listes.
- Journal prévu pour 200 interventions.
- Six statuts, priorités, dates, intervenants, compte rendu et durée.
- Identifiants en double signalés, sans blocage.
- Démonstration recalculée : 6 interventions, une dans chacun des six statuts, 1 urgente non terminée, 0 doublon et 2 heures.

### Suivi de maintenance v1.0
- Feuilles : Guide, Interventions, Équipements, Tableau de bord, Listes.
- Capacité de conception : 100 équipements et 500 interventions.
- Prochaine échéance calculée à partir de la dernière maintenance préventive et de la périodicité en jours.
- La date de dernière préventive doit être actualisée manuellement dans Équipements ; le journal Interventions ne la synchronise pas.
- Ce classeur n'est pas une GMAO.
- Démonstration recalculée : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions, 5 heures, 0 doublon et 0 fiche à compléter.

## Offres affichées sur le site

Les tarifs ci-dessous sont des prix de lancement affichés pour un besoin simple et un périmètre défini. Les offres sont des créations à la demande, pas des fichiers immédiatement téléchargeables. Le contenu, le format, la faisabilité et le prix doivent être confirmés avant toute réalisation.

| Offre | Prix de lancement affiché |
|---|---:|
| Tableau simple | 15 € |
| Suivi de stock | 20 € |
| Registre d'interventions | 25 € |
| Suivi de maintenance | 25 € |
| Tableau de bord | Dès 40 € |
| Besoin spécifique | Sur devis |

Le suivi de stock, le registre d'interventions et le suivi de maintenance sont présentés comme prototypes en préparation et non disponibles à la livraison tant que les contrôles restants ne sont pas terminés.

## Prospection nationale

Le fichier `suivi-prospection.csv` contient 27 entreprises distinctes dans 18 territoires (13 régions métropolitaines et 5 DROM). Il comporte 17 colonnes, une URL source par entreprise, 15 e-mails publics et 24 téléphones publics recensés. Le contrôle structurel du 17/11/2026 confirme : aucune ligne mal formée, aucun doublon, aucun besoin marqué confirmé et aucun contact marqué comme effectué.

Les dates de recherche vont du 05/11 au 15/11/2026. Le contrôle du 17/11 est structurel et ne revalide pas individuellement chaque coordonnée. Avant toute démarche, vérifier à nouveau la page officielle, le rôle du destinataire, le canal approprié et toute opposition. Ne jamais utiliser un numéro d'urgence ou de dépannage comme canal commercial.

- [Liste nationale des prospects et sources](premiers-prospects.md)
- [Suivi de prospection CSV](suivi-prospection.csv)
- [Grille de qualification nationale](grille-qualification-prospects-nationale.md)

## Documents de travail

- [Cahier des charges du stock](modele-suivi-stock-specification.md)
- [Cahier des charges du registre d'interventions](modele-registre-interventions-specification.md)
- [Cahier des charges du suivi de maintenance](modele-suivi-maintenance-specification.md)
- [Grille de contrôle qualité des tableurs](grille-controle-qualite-tableurs.md)
- [Fiche de cadrage client](fiche-cadrage-client.md)
- [Plan de développement](plan-de-developpement.md)
- [Brouillons de mentions légales et confidentialité](brouillon-mentions-legales-confidentialite.md)

## Points bloquants

- Les tests interactifs dans l'interface de LibreOffice Calc et un test utilisateur extérieur restent à faire.
- Excel n'a pas été testé.
- Les doublons sont détectés, mais pas bloqués.
- Les mentions légales et la politique de confidentialité ne sont pas publiées : les informations exactes de l'exploitant et les vérifications nécessaires manquent. Ne pas inventer ni publier de coordonnées juridiques.
- Les binaires ODS ne sont pas publiés dans le dépôt public.

## Garde-fous

- Aucun e-mail commercial, appel ou formulaire envoyé.
- Aucune dépense engagée.
- Aucun engagement juridique pris.
- Les exemples de tableurs sont fictifs.
- Aucun besoin de prospect n'est présenté comme confirmé sans preuve.
