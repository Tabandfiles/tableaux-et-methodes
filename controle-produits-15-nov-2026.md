# Contrôle produits, site et prospection — 15 novembre 2026

## État du dépôt et du site

- Dépôt public : [Tabandfiles/tableaux-et-methodes](https://github.com/Tabandfiles/tableaux-et-methodes), branche `main`, droits de lecture/écriture confirmés.
- Arborescence contrôlée : 24 fichiers ; aucun binaire ODS/XLSX n'est publié dans le dépôt.
- Site public relu en direct : [Tableaux & Méthodes](https://tabandfiles.github.io/tableaux-et-methodes/). La portée nationale, les six offres, les prix de lancement, les exemples fictifs, les liens e-mail et le statut « stock en préparation » sont visibles.
- `robots.txt` et `sitemap.xml` sont accessibles ; le sitemap ne référence que la page d'accueil, seule page HTML publique actuelle.
- Déploiement final du 15/11/2026 : workflow Pages n° 43746840172, terminé avec succès (conclusion `success`) pour le commit `486d2a0f8ab52aedcec14b730ec7ef3dd50aa2fa`. Le site public a ensuite été relu : nouveau titre, description Open Graph et couleur de thème visibles. Le sitemap affiche `lastmod` au 15/11/2026.

## Suivi de stock ODS v2.2 — prototype de travail

Deux fichiers locaux ont été créés à partir de la v2.1 :

- `Tableaux_Methodes_Suivi_Stock_demo_v2_2.ods` — démonstration fictive.
- `Tableaux_Methodes_Suivi_Stock_vierge_v2_2.ods` — version vierge.

Chaque fichier contient cinq feuilles et 507 cellules de formule. La capacité de conception reste de 100 références et 500 mouvements. Le filtre de Stock couvre maintenant A1:N101, avec une colonne « Contrôle réf. » qui signale les références dupliquées. Cette alerte est informative et ne bloque pas la saisie.

Tests recalculés dans LibreOffice Calc :

| Cas | Résultat |
|---|---|
| Gants nitrile | Stock 8 ; alerte À COMMANDER |
| Nettoyant | Stock 24 ; alerte OK |
| Joint 20 mm | Stock 3 ; alerte À COMMANDER |
| Tableau de bord | 3 références ; 2 alertes ; 1 OK ; 4 mouvements ; 35 unités ; 0 doublon |
| Scénario de doublon injecté | Les deux lignes sont signalées DOUBLON ; compteur = 2 |
| Version vierge | Tous les indicateurs à zéro |

Les sept règles de validation présentes ont été relues via l'interface UNO de LibreOffice : listes de référence/type/motif/catégorie et contrôles numériques, avec alerte bloquante configurée. Les filtres sont définis dans les plages du classeur. Cela ne remplace pas un test au clic dans l'interface graphique.

## Registre d'interventions ODS v1.0 — nouveau prototype

Deux fichiers locaux ont été créés :

- `Tableaux_Methodes_Registre_Interventions_demo_v1_0.ods` — six lignes fictives.
- `Tableaux_Methodes_Registre_Interventions_vierge_v1_0.ods` — version vierge.

Chaque fichier contient quatre feuilles (Guide, Interventions, Tableau de bord, Listes), 210 cellules de formule, quatre règles de validation, un AutoFiltre A1:R201 et une capacité de conception de 200 interventions. La colonne « Contrôle ID » signale les numéros en double ; elle ne bloque pas la saisie.

Résultats recalculés dans LibreOffice : 6 interventions, une dans chacun des six statuts, une urgente non terminée, zéro doublon et 2 heures enregistrées. Un scénario avec deux identifiants identiques signale les deux lignes et affiche un compteur de 2. Un test en ligne 201 confirme que la dernière ligne prévue est incluse dans les calculs. La version vierge affiche zéro.

Les listes déroulantes Type, Priorité et Statut et la validation de durée non négative ont été relues via UNO avec une alerte de type STOP. Les dates sont typées et formatées comme dates, mais aucune validation stricte de date n'est activée. Le rendu PDF a été contrôlé : quatre pages, dont la feuille Interventions en A3 paysage.

## Limites restantes avant commercialisation

- Le clic réel sur les listes déroulantes, les filtres et les messages de refus n'a pas été testé dans une session graphique interactive.
- Les références/identifiants en doublon sont signalés mais pas bloqués.
- Aucun test utilisateur externe n'a été réalisé.
- Excel n'a pas été testé.
- Le suivi de maintenance n'a toujours pas de classeur ODS construit.
- Les mentions légales et la politique de confidentialité restent des brouillons incomplets, à ne pas publier avant ajout des informations exactes de l'exploitant et vérification.

Les binaires ODS et les PDF de prévisualisation restent des livrables locaux de travail ; ils ne sont pas ajoutés au dépôt public ni proposés au téléchargement sur le site à ce stade.

## Prospection nationale

Le CSV conserve 27 entreprises distinctes sur 18 territoires (13 régions métropolitaines et 5 DROM), 17 colonnes, aucune ligne mal formée et aucune entreprise en doublon. Cinq coordonnées ont été revalidées le 15/11/2026 sur des pages officielles : A2L Chauffage Plomberie (Normandie), S-BEC (Bretagne), Plomberie du Haut Berry (Centre-Val de Loire), Clean Plomberie (Martinique) et MLP Plomberie Chauffage (Auvergne-Rhône-Alpes). Les sources et les réserves sont dans `premiers-prospects.md` et `suivi-prospection.csv`.

Aucun besoin n'est confirmé, aucun contact n'est marqué comme effectué et aucun message n'a été envoyé.

## Garde-fous

Aucun e-mail commercial envoyé, aucun appel ni formulaire envoyé, aucune dépense engagée et aucun engagement juridique pris.


## Vérification finale — 15 novembre 2026, 19 h

Les quatre classeurs ODS ont été rouverts et contrôlés après les réglages d'impression. Les nombres de formules sont inchangés (507 pour chacun des deux suivis de stock, 210 pour chacun des deux registres d'interventions). Les règles de validation et les plages de filtre sont présentes dans les fichiers finaux. Les quatre PDF de prévisualisation ont été générés et vérifiés : 6 pages par fichier de stock, 4 pages par fichier d'interventions. Le contrôle final confirme les calculs, les versions vierges à zéro et les scénarios de doublons. Aucun fichier ODS/PDF n'a été ajouté au dépôt public.
