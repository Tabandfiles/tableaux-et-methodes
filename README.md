# Tableaux & Méthodes

Création de tableaux de suivi simples pour artisans, petites entreprises, associations et équipes de maintenance, avec une priorité donnée à LibreOffice Calc. Les demandes sont traitées à distance partout en France.

- **Site public :** https://tabandfiles.github.io/tableaux-et-methodes/
- **Contact :** tabsandmethod@gmail.com
- **État du suivi de stock au 14/11/2026 :** prototype ODS v2.1 reconstruit localement, 5 feuilles et 406 formules ; filtres et validations configurés, tests dynamiques et limites documentés. Pas encore livrable commercial : contrôle interactif dans Calc et test utilisateur restent à faire. Les binaires ne sont pas publiés dans le dépôt.
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
- [Prospection nationale](premiers-prospects.md) — 27 pistes : 22 en métropole réparties dans les 13 régions métropolitaines et 5 dans les DROM ; 18 territoires couverts ; besoins non confirmés ; aucun contact envoyé.
- [Suivi de prospection](suivi-prospection.csv) — modèle de suivi des prises de contact.
- [Modèles d'e-mails](modeles-emails-prospection.md) — brouillons uniquement, aucun message envoyé.
- [Fiche de cadrage client](fiche-cadrage-client.md) — questions pour définir le besoin, le volume, le logiciel et le périmètre avant devis.
- [Plan de développement](plan-de-developpement.md) — plan de validation commerciale.
- [Brouillons juridiques](brouillon-mentions-legales-confidentialite.md) — incomplets, ne pas publier avant ajout des informations réelles et vérification.

## Priorités

1. Faire un contrôle interactif des listes déroulantes, filtres et messages de validation dans l'interface LibreOffice Calc.
2. Ajouter un contrôle des références en double et vérifier les saisies par copier-coller.
3. Faire tester le prototype par une personne non technique et corriger les points de friction.
4. Finaliser le rendu d'impression et confirmer le périmètre commercial avant toute livraison.
5. Créer ensuite les fichiers ODS du registre d'interventions et du suivi de maintenance.
6. Compléter les pages juridiques avec les informations exactes de l'exploitant avant publication.
7. Revalider les coordonnées et les canaux des entreprises juste avant toute prise de contact.

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


## Mise à jour nationale — 13 novembre 2026

Le fichier de prospection contient désormais **27 entreprises distinctes** sur 18 territoires (13 régions métropolitaines et 5 DROM), avec 17 colonnes et aucune ligne dupliquée. Quatre nouvelles pistes ont été ajoutées après vérification des pages officielles : S-BEC (Bretagne), Plomberie du Haut Berry (Centre-Val de Loire), Hiviaco (Grand Est) et GB Climatisation (Corse). Les besoins restent inconnus ; aucun contact n'a été effectué.

Les fichiers `robots.txt` et `sitemap.xml` sont présents dans le dépôt et leur publication a été vérifiée sur le site public. Le sitemap ne référence que la page d'accueil, seule page HTML publique actuelle.


## Contrôle prototype ODS v2.1 — 14 novembre 2026

Deux fichiers de travail ont été reconstruits localement et recalculés avec LibreOffice Calc : une démonstration avec données fictives et une version vierge. Chaque fichier comporte les cinq feuilles Guide, Mouvements, Stock, Tableau de bord et Listes, avec 406 cellules de formule.

- Capacité de conception : 100 références (Stock lignes 2 à 101) et 500 mouvements (Mouvements lignes 2 à 501). Le test de frontière a utilisé la 100e référence et le 500e mouvement.
- Validations configurées : référence de mouvement choisie dans Stock, type Entrée/Sortie, motif, catégorie, quantité de mouvement strictement positive, stock initial et seuil positifs ou nuls.
- Filtres automatiques configurés sur les en-têtes de Stock et Mouvements.
- Les lignes Stock sans référence restent visuellement vides au lieu d'afficher des zéros. La colonne L est nommée Date inventaire.
- Mise en page PDF contrôlée : démonstration 5 pages ; version vierge 6 pages. Stock en A3 paysage avec répétition de l'en-tête ; mouvements en A4 paysage.
- Tests recalculés : stock GNT-001 = 8, CLN-002 = 24, JNT-003 = 3 ; tableau de bord = 3 références, 2 alertes, 0 négatif, 1 OK, 4 mouvements, 35 unités.
- Seuil exact : stock 3 avec seuil 3, alerte À COMMANDER. Stock négatif : -1, alerte STOCK NÉGATIF et compteur négatif = 1. Frontière : référence 100 et mouvement 500 calculés correctement.
- Version vierge : tous les indicateurs du tableau de bord sont à zéro.

Les deux binaires restent des fichiers de travail locaux et ne sont pas publiés dans le dépôt. Les tests ont été faits avec LibreOffice en mode sans interface et par export PDF ; le clic réel dans les listes/filtres, les messages de validation en interaction, Excel et un test utilisateur ne sont pas encore validés. Les références en double ne sont pas encore bloquées automatiquement. Voir le rapport [contrôle du 14 novembre](controle-prototype-suivi-stock-14-nov-2026.md).

## Mise à jour des livrables — 15 novembre 2026

- **Suivi de stock ODS v2.2** : démonstration et version vierge créées localement ; 5 feuilles, 507 cellules de formule, filtre Stock A1:N101 et alerte informative de références dupliquées. Les fichiers ne sont pas publiés dans le dépôt.
- **Registre d'interventions ODS v1.0** : démonstration et version vierge créées localement ; 4 feuilles, 200 lignes prévues, 210 cellules de formule, 4 règles de validation, filtre A1:R201 et alerte informative d'identifiants dupliqués. Les fichiers ne sont pas publiés dans le dépôt.
- Les deux prototypes ont été recalculés avec LibreOffice sur des scénarios fictifs. Les validations et alertes STOP ont été relues via UNO. Le clic réel sur les listes/filtres, un test utilisateur et Excel restent à faire ; aucun produit n'est déclaré prêt à la vente.
- Cinq coordonnées de prospection ont été revalidées sur les sites officiels le 15/11/2026. La liste conserve 27 pistes dans 18 territoires ; tous les besoins restent inconnus et aucun contact n'a été effectué.
- Voir [le rapport de contrôle du 15 novembre](controle-produits-15-nov-2026.md).


Complément qualité du 15/11/2026 : le registre d'interventions v1.0 comporte désormais une validation de date de type DATE (1900–9999) avec alerte STOP sur les quatre colonnes de dates. Cinq règles sont présentes dans chaque fichier final.
