# Contrôle du projet Tableaux & Méthodes — 27 novembre 2026

## Dépôt GitHub

- Dépôt : [Tabandfiles/tableaux-et-methodes](https://github.com/Tabandfiles/tableaux-et-methodes)
- Visibilité : public.
- Branche par défaut : `main`.
- Accès de modification disponible pour le dépôt.
- Dernier commit observé avant cette mise à jour : `adbdccf006e5bc64d1f41772b2c8743d6b1e0c3a` (26/11/2026).
- Aucun statut CI n'était attaché à ce commit au moment du contrôle ; ne pas assimiler l'absence de statut à un workflow réussi.

## Site public

Pages consultées le 27/11/2026 :

- [Accueil](https://tabandfiles.github.io/tableaux-et-methodes/) : accessible ; présente la création à distance partout en France et précise que seule l'offre Tableau simple (15 € affichés, après cadrage) est ouverte à la demande. Les prototypes Stock, Interventions et Maintenance sont explicitement indiqués comme non disponibles à la livraison.
- [Catalogue PDF](https://tabandfiles.github.io/tableaux-et-methodes/catalogue.pdf) : accessible ; document informatif daté du 25/11/2026, avec les états de disponibilité et les limites des offres.
- [Aperçu PDF du suivi des demandes](https://tabandfiles.github.io/tableaux-et-methodes/exemples/suivi-demandes-apercu.pdf) : accessible ; six demandes fictives, format ODS annoncé, capacité prévue de 50 lignes et limites clairement indiquées.

Aucune modification du code du site n'a été nécessaire le 27/11 : les informations vérifiées sont cohérentes. Aucun nouveau déploiement Pages n'est revendiqué pour cette session.

## Contrôle de la base de prospection

Contrôle du CSV avant ajout : 42 entreprises, 17 colonnes par ligne, 18 territoires, 29 e-mails publics, 40 téléphones publics, aucun doublon, aucun besoin confirmé et aucun contact effectué.

### Nouvelle piste ajoutée

**SANCYTI — La Chevrolière, Pays de la Loire**

- Activité publiée : plomberie, chauffage, climatisation, ventilation et rénovation énergétique ; clientèle de particuliers et de professionnels.
- E-mail professionnel publié : `contact@sancyti.fr`.
- Téléphone publié : `06 37 40 33 51`.
- Sources officielles : [page Contact](https://sancyti.fr/contact/) et [site](https://sancyti.fr/), consultés le 27/11/2026.
- La page Contact indique les horaires du lundi au vendredi, 8h–18h.
- Taille, organisation interne, outils de suivi et rôle du destinataire : inconnus.
- Besoin de tableur : **non confirmé**.
- Contact effectué : **non**.

Après ajout : **43 entreprises distinctes**, 18 territoires, 30 e-mails publics, 41 téléphones publics, 17 colonnes par ligne, aucun doublon, aucun besoin confirmé, aucun contact effectué.

## Modifications effectuées dans le dépôt

- `suivi-prospection.csv` : ajout de SANCYTI avec sources officielles, statut de besoin inconnu et contact non effectué.
- `premiers-prospects.md` : mise à jour de l'en-tête et ajout de la fiche sourcée du 27/11.
- `grille-qualification-prospects-nationale.md` : mise à jour des compteurs et de la date de référence.
- `README.md` : état du projet et indicateurs nationaux actualisés.

## Limites et prochaine priorité

- Les coordonnées des pistes plus anciennes doivent être revérifiées individuellement avant toute éventuelle démarche.
- Aucun test interactif à la souris du Tableau simple n'a été réalisé dans cette session.
- Aucun testeur extérieur, test Excel ou essai d'impression physique n'est déclaré.
- Les classeurs ODS ne sont pas publiés comme produits téléchargeables ; les prototypes automatisés restent indisponibles à la livraison.
- Les informations exactes de l'exploitant manquent toujours pour finaliser les mentions légales.

**Prochaine priorité :** obtenir une recette interactive du Tableau simple dans LibreOffice Calc (listes, refus des valeurs non autorisées, filtres, tri et copier-coller), puis faire exécuter le guide par un testeur extérieur. En parallèle, continuer à qualifier la base nationale sans présumer des besoins.

Aucun e-mail commercial envoyé, aucun appel passé, aucun formulaire soumis, aucune dépense engagée et aucun engagement juridique pris.


## Vérification complémentaire du pack Tableau simple v1.1

L'archive de travail locale `Tableaux_Methodes_Tableau_Simple_v1_1_25-11-2026.zip` a été ouverte sans modification des originaux. Résultats observés le 27/11/2026 :

- Intégrité de l'archive ZIP : OK.
- Deux fichiers ODS présents : démonstration et vierge.
- Chaque ODS contient les feuilles Guide, Suivi et Listes.
- Deux définitions de validation (Priorité et Statut) et 100 références de cellules à validation par fichier.
- Plages d'impression : Guide A1:F12 et Suivi A1:I12 pour la démonstration ; Guide A1:F12 et Suivi A1:I54 pour le fichier vierge.
- Conversion LibreOffice en mode sans interface vers PDF : 2 pages A4 pour la démonstration et 3 pages A4 pour le fichier vierge.

Ces vérifications confirment l'intégrité, l'ouverture et la conversion des fichiers dans l'environnement testé. Elles ne prouvent pas le comportement des menus déroulants au clic ni le refus des valeurs interdites. Les filtres, le tri, le copier-coller manuel, le test par une personne extérieure, Excel et l'impression physique restent à tester.

## Commits de mise à jour

- [Ajout de SANCYTI au CSV](https://github.com/Tabandfiles/tableaux-et-methodes/commit/083463136be0f446ad1e6cee79514fd6761136a3)
- [Actualisation du dossier national](https://github.com/Tabandfiles/tableaux-et-methodes/commit/917c6f883f4789a0c129159cae2d9f23b186ae02)
- [Mise à jour de la grille de qualification](https://github.com/Tabandfiles/tableaux-et-methodes/commit/62950fb6948a3eb18bc7dbf59f7211cc81d60736)
- [Actualisation du README](https://github.com/Tabandfiles/tableaux-et-methodes/commit/882332d2c960abc826ba0b4488350256a3aaf5a0)
- [Création du présent rapport](https://github.com/Tabandfiles/tableaux-et-methodes/commit/738b5aea0e9cdf58e56fb9d0b5ae1d65adaa0c4a)
