# Tableaux & Méthodes

Création de tableaux de suivi simples pour artisans, petites entreprises, associations et équipes de maintenance, avec une priorité donnée à LibreOffice Calc. Les demandes sont traitées à distance partout en France.

- **Site public :** https://tabandfiles.github.io/tableaux-et-methodes/
- **Contact :** tabsandmethod@gmail.com
- **Pas d'abonnement :** le périmètre et le prix doivent être confirmés avant toute réalisation.

## Offres affichées sur le site

| Offre | Prix de lancement affiché |
|---|---:|
| Tableau simple | 15 € |
| Suivi de stock | 20 € |
| Registre d'interventions | 25 € |
| Suivi de maintenance | 25 € |
| Tableau de bord | Dès 40 € |
| Besoin spécifique | Sur devis |

Ces tarifs sont des prix de lancement pour un périmètre défini. Ils ne signifient pas qu'un fichier prêt à télécharger est disponible pour chaque offre.

## État réel des livrables

- [Fiche produit — suivi de stock](fiche-produit-suivi-stock.md) — périmètre de base et limites de l'offre à 20 €.
- [Cahier des charges du suivi de stock](modele-suivi-stock-specification.md) — le journal interne documente un ODS v2.1 recalculé avec LibreOffice Calc ; 5 feuilles, 405 formules, 100 références et 500 mouvements prévus.
- [Journal de tests ODS v2.1](tests-suivi-stock-v2-1.md) — tests statiques et dynamiques réussis sur données fictives : stocks 8, 24 et 3 ; tableau de bord 3 références, 2 alertes, 1 OK, 4 mouvements, 35 unités ; seuil exact et stock négatif testés.
- **Contrôle du livrable joint le 9 novembre :** le seul fichier réellement disponible dans l'espace de travail de cette vérification est `Tableaux_Methodes_Suivi_Stock_v1.ods` (32 910 octets). Il s'agit d'une ancienne maquette : 5 feuilles, 6 formules dans Stock, 5 dans le tableau de bord ; les entrées/sorties cumulées sont saisies manuellement et le journal Mouvements ne met pas le stock à jour. Ne pas la présenter comme la v2.1 ni comme le produit final. Le fichier v2.1 décrit dans les journaux n'est pas présent dans cet espace de travail et ne peut donc pas être joint ou recontrôlé ici. Voir [l'audit du livrable](controle-livrable-suivi-stock-9-nov-2026.md).
- Le fichier ODS v2.1 n'est pas publié dans le dépôt public afin de ne pas rendre le modèle commercial complet librement téléchargeable. Excel n'a pas été testé.
- Limites restantes du stock : menus déroulants non configurés, filtres à vérifier visuellement dans Calc, quantités négatives non bloquées à la saisie, références inconnues ou dupliquées non détectées, test utilisateur à réaliser.
- [Cahier des charges du registre des interventions](modele-registre-interventions-specification.md) — spécification écrite ; fichier ODS final non créé et formules non testées.
- [Cahier des charges du suivi de maintenance](modele-suivi-maintenance-specification.md) — conception version 1 définie ; fichier ODS non créé et formules non testées.
- [Grille de contrôle qualité](grille-controle-qualite-tableurs.md) — critères et journaux de tests.
- [Contrôle du site public](controle-site-public-9-nov-2026.md) — SEO, liens de contact, portée nationale et absence actuelle de pages juridiques publiées.
- [Prospection nationale](premiers-prospects.md) — 23 pistes : 18 en métropole réparties dans les 13 régions métropolitaines et 5 pistes dans les DROM ; les nouvelles pistes ultramarines ont été vérifiées sur les sites officiels le 12 novembre ; besoins non confirmés ; aucun contact envoyé.
- [Suivi de prospection](suivi-prospection.csv) — modèle de suivi des prises de contact.
- [Modèles d'e-mails](modeles-emails-prospection.md) — brouillons uniquement, aucun message envoyé.
- [Fiche de cadrage client](fiche-cadrage-client.md) — questions pour définir le besoin, le volume, le logiciel et le périmètre avant devis.
- [Plan de développement](plan-de-developpement.md) — plan de validation commerciale.
- [Brouillons juridiques](brouillon-mentions-legales-confidentialite.md) — incomplets, ne pas publier avant ajout des informations réelles et vérification.

## Priorités

1. Récupérer dans l'espace de travail le véritable ODS v2.1 décrit dans le journal de tests ; à défaut, reconstruire le livrable après levée du blocage de génération.
2. Ne pas remettre la maquette v1 comme produit automatisé : ses cumuls sont manuels.
3. Vérifier visuellement les filtres dans LibreOffice Calc, ajouter et tester les validations de saisie, puis créer une copie vierge.
4. Faire tester le modèle par une personne non technique et corriger les points de friction.
5. Développer ensuite le registre d'interventions et le suivi de maintenance, sans annoncer de fichiers non créés.
6. Compléter les mentions légales avec les informations exactes de l'exploitant avant publication.
7. Revalider les coordonnées des prospects juste avant tout contact ; la présence d'un contact public ne confirme aucun besoin.

## Vérification du site et du dépôt — 9 novembre 2026

- Le dépôt `Tabandfiles/tableaux-et-methodes` est public, la branche par défaut est `main`, les droits de modification sont disponibles.
- Le site public a été relu en direct : portée nationale, offres, exemples fictifs, FAQ et contact sont accessibles.
- Le workflow Pages n° 63, associé au commit `20cd504`, a terminé avec succès : les trois jobs build, report-build-status et deploy sont réussis. Le site public a ensuite été relu et affiche bien la mention de finalisation du suivi de stock : https://github.com/Tabandfiles/tableaux-et-methodes/actions/runs/42680596675.
- Le contrôle HTML a relevé 9 liens e-mail utilisant tous `tabsandmethod@gmail.com`, les métadonnées SEO attendues et l'absence de liens vers des mentions légales/confidentialité publiées. Voir [le contrôle du site](controle-site-public-9-nov-2026.md).

## Contrôle du site — 11 novembre 2026

- Une correction a été apportée à `index.html` : le suivi de stock automatisé est désormais présenté comme **en préparation et non disponible à la livraison**. Les 100 références et 500 mouvements sont explicitement une cible de conception, non une capacité garantie.
- Les premiers workflows déclenchés par ces commits ont été annulés à la suite de modifications successives ; le workflow du dernier commit était encore en attente lors du dernier contrôle. La page publique renvoyait encore l'ancien texte. Ne pas déclarer la correction publiée avant la fin d'un déploiement du dernier commit et une nouvelle lecture de la page en ligne.
- Le contrôle détaillé et les références des workflows sont consignés dans [le rapport du 11 novembre](controle-site-public-11-nov-2026.md).
- Trois coordonnées professionnelles ont été revalidées le 11 novembre sur les sites officiels d'A2L Chauffage Plomberie (Normandie), SBE (Bourgogne-Franche-Comté) et CMH Industrie (Provence-Alpes-Côte d’Azur) ; voir [la liste nationale](premiers-prospects.md). Aucun contact n'a été envoyé.
- Le binaire ODS v2.1 n'est toujours pas présent dans le dépôt. Le prototype v1 reste une maquette à cumuls manuels.

## Principes

- Aucun e-mail commercial envoyé sans décision explicite.
- Aucune dépense ni engagement juridique pris.
- Coordonnées de prospection sourcées sur les pages officielles quand possible.
- Ne jamais annoncer un modèle, une formule ou une compatibilité comme testé si ce n'est pas le cas.


## Inventaire des anciens modèles — 10 novembre 2026

Une inspection en lecture seule de la bibliothèque a retrouvé deux anciens classeurs XLSX : `pack_modeles_suivi_numerique.xlsx` (5 feuilles, 105 formules, validations de données sur certaines colonnes) et `modele_suivi_maintenance_demo.xlsx` (3 feuilles, 52 formules). Ils peuvent servir de références de conception, mais ne sont pas des fichiers ODS validés dans LibreOffice. Le pack Stock ne contient pas de journal de mouvements automatisé. Voir [l'inventaire détaillé](inventaire-modeles-existants-10-nov-2026.md).

La recherche n'a pas retrouvé le binaire `Tableaux_Methodes_Suivi_Stock_v2_1.ods` dans la bibliothèque, les fichiers de conversation ni l'arborescence du dépôt. Le fichier v1 reste la seule maquette stock remise dans la conversation et ne doit pas être vendu comme modèle automatisé.


## Vérification du projet — 12 novembre 2026

- Le dépôt public est sur la branche `main`, au commit `08bf66bd4ff1cea40dc44331c52e96ede7fa55ef` avant les mises à jour documentaires de cette journée.
- L'arborescence publique contient 19 fichiers ; aucun binaire ODS ou XLSX n'y est présent. Le journal de tests v2.1 et sa fiche produit sont des documents de suivi, pas le classeur lui-même.
- Après les modifications du 12 novembre, le workflow Pages n° 83 s'est terminé avec succès. La page publique a été relue et sert bien les nouveaux libellés « Décrire mon besoin » et la précision indiquant que les offres sont des créations à la demande. Le workflow n° 84, déclenché par la correction du CSV, s'est également terminé avec succès. Le workflow n° 86, déclenché par les dernières mises à jour documentaires, a terminé ses trois étapes build, report-build-status et deploy avec succès.
- Les offres sont désormais présentées explicitement comme des créations à la demande, et les liens des cartes invitent à décrire un besoin plutôt qu'à demander un fichier prêt à télécharger.
- La prospection comprend 23 pistes recensées : 18 en métropole et 5 dans les DROM. Les cinq nouvelles pistes sont sourcées par des pages officielles ; aucun besoin n'est confirmé et aucun contact n'a été effectué.
- Les brouillons de mentions légales et de confidentialité restent incomplets. Ne pas les publier sans les informations réelles de l'exploitant et les vérifications nécessaires.


Le CSV de prospection a été contrôlé après correction : 23 lignes d'entreprises, 17 colonnes par ligne, aucune entreprise en doublon. Le dernier contrôle du site public confirme la mise en ligne des nouveaux textes.


## Contrôle du prototype de stock — 13 novembre 2026

Un prototype local **v2.0** a maintenant été créé et recalculé avec LibreOffice Calc : cinq feuilles, 406 formules, 100 références et 500 mouvements prévus. Les exemples fictifs donnent 8, 24 et 3 unités ; le tableau de bord affiche 3 références, 2 alertes, 1 référence OK, 4 mouvements et 35 unités. Trois cas dynamiques (sortie augmentée, seuil exact, stock négatif) et une version vierge ont été contrôlés. **Ce prototype n'est pas encore prêt à la vente** : filtres manuels, menus déroulants et contrôles de saisie restent à finaliser ; rendu avec interface Calc et compatibilité Excel non testés. Les deux binaires restent des fichiers de travail non publiés dans le dépôt. Voir [le rapport de contrôle du 13 novembre](controle-prototype-suivi-stock-13-nov-2026.md).


**Contrôle de mise en page :** l'export PDF A4 du prototype a révélé une colonne Date trop étroite (`###`) et une feuille Stock qui ne tient pas proprement sur une seule largeur de page. L'impression n'est pas validée ; une vérification dans Calc avec interface et une correction de mise en page restent nécessaires.
