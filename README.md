# Tableaux & Méthodes

Création à distance de tableaux de suivi sur mesure pour artisans, petites entreprises, associations et équipes de maintenance, partout en France. Les modèles sont conçus en priorité pour LibreOffice Calc.

- **Site public :** https://tabandfiles.github.io/tableaux-et-methodes/
- **Contact :** tabsandmethod@gmail.com
- **Dépôt :** https://github.com/Tabandfiles/tableaux-et-methodes

## État du projet au 26 novembre 2026

Le 25/11/2026, le Tableau simple a été porté en v1.1 après découverte d'une zone d'impression trop courte dans la version vierge : elle s'arrêtait à A1:I24 et n'imprimait que 20 lignes. La zone a été étendue à A1:I54 ; le nouvel export PDF montre les 50 lignes prévues sur deux pages de tableau. Le pack de contrôle v1.1 reste local au projet et n'est pas publié en téléchargement public. Les essais interactifs au clic, le test utilisateur extérieur, Excel et l'impression physique restent à réaliser.

Trois familles de prototypes ODS existent en démonstration fictive et en version vierge. Les six fichiers de travail sont conservés hors du dépôt public et regroupés dans l'archive locale `Tableaux_Methodes_Prototypes_21-11-2026.zip`. Le catalogue PDF informatif, actualisé le 25/11/2026 avec un tableau de disponibilité explicite, est publié dans `catalogue.pdf`.

| Produit | Version | Feuilles | Formules par fichier | Validations | Filtres | Capacité de conception |
|---|---:|---:|---:|---:|---:|---|
| Suivi de stock | v2.2 | 5 | 507 | 7 | 2 | 100 références / 500 mouvements |
| Registre d'interventions | v1.0 | 4 | 210 | 5 | 1 | 200 interventions |
| Suivi de maintenance | v1.1 | 5 | 508 | 9 | 2 | 100 équipements / 500 interventions |

Le 19/11/2026, les trois familles ont fait l'objet de tests fonctionnels via LibreOffice Calc (UNO) sur des copies temporaires : mouvements et alertes du stock, mise à jour du tableau de bord du registre, détection des doublons et synchronisation automatique de la dernière maintenance préventive depuis le journal. Les filtres et règles de validation ont été inspectés. Les six classeurs du pack ont été recalculés et contrôlés ; aucune erreur de formule visible n'a été détectée dans le XML. Le 20/11/2026, une incohérence de données fictives a été corrigée dans la démonstration maintenance : VAN-003 possède maintenant l'intervention préventive réalisée du 10/11/2026 qui alimente la date et l'échéance affichées. Des tests temporaires confirment qu'une préventive plus récente met à jour la date et qu'une corrective ultérieure ne la modifie pas.

**Le 21/11/2026, la recette d’impression PDF a mis en évidence puis corrigé des zones qui couvraient des centaines de lignes vides : les six classeurs exportent désormais chacun 5 pages non vides. Les guides et notes de tableaux de bord sont renvoyés à la ligne ; le journal du registre est imprimé en deux panneaux ; les vues imprimées Stock et Équipements conservent les colonnes principales. Le rappel du tableau de bord Maintenance a été corrigé. L’impression physique reste à tester.

Aucun de ces prototypes n'est déclaré prêt à la vente.** Les clics réels dans l'interface graphique de Calc, les messages de validation, le copier-coller, l'impression et un test utilisateur extérieur restent à vérifier. Excel n'a pas été testé. Les doublons sont signalés mais non bloqués.

Voir le [rapport de contrôle du 17 novembre](controle-prototypes-17-nov-2026.md), le [contrôle maintenance v1.1 du 19 novembre](controle-suivi-maintenance-v1-1-19-nov-2026.md), le [contrôle de cohérence maintenance du 20 novembre](controle-maintenance-20-11-2026.md), les [tests de calcul des trois classeurs du 20 novembre](controle-calculs-classeurs-20-nov-2026.md), le [contrôle du site du 20 novembre](controle-site-20-nov-2026.md) et le [plan de recette manuelle](plan-recette-acceptation-ods.md).

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

### Suivi de maintenance v1.1
- Feuilles : Guide, Interventions, Équipements, Tableau de bord, Listes.
- Capacité de conception : 100 équipements et 500 interventions.
- La dernière préventive est calculée automatiquement depuis le journal : même ID, type `Préventive`, résultat `Réalisée` ; la date la plus récente est retenue.
- La prochaine échéance est calculée à partir de cette date et de la périodicité en jours. Une corrective ou une préventive non réalisée ne repousse pas l'échéance.
- Ce classeur n'est pas une GMAO.
- Démonstration : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions, 5 heures, 0 doublon et 0 fiche à compléter.

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

Le suivi de stock, le registre d'interventions et le suivi de maintenance sont présentés comme prototypes en préparation et non disponibles à la livraison tant que les contrôles restants ne sont pas terminés. Les montants correspondants sont indicatifs et ne signifient pas que ces produits sont commandables.

## Prospection nationale

Le fichier `suivi-prospection.csv` contient 42 entreprises distinctes dans 18 territoires (13 régions métropolitaines et 5 DROM). Il comporte 17 colonnes, une URL source par entreprise, 29 e-mails professionnels publics et 40 entreprises disposant d'au moins un numéro de téléphone publié. Le contrôle structurel du 26/11/2026 confirme : 42 entreprises distinctes, 17 colonnes, une URL source par ligne, aucune ligne mal formée, aucun doublon, aucun besoin marqué confirmé et aucun contact marqué comme effectué.

Les dates de recherche vont du 05/11 au 26/11/2026. Quatre pistes supplémentaires (Anthony OLIVEIRA, Aquitaine Plomberie 3 Étoiles, APSC Azur Plomberie Sanitaire et Chauffage, I.D.PLOMBERIE) ont été ajoutées le 18/11 à partir de leurs pages officielles ; deux pages consultées portent des dates anciennes et doivent être revalidées avant toute démarche. Deux pistes supplémentaires (RS Chauffage, Grand Est ; Aquitaine Energies Plomberie, Nouvelle-Aquitaine) ont été vérifiées le 19/11 sur leurs pages officielles. Une piste V.I.C. Plomberie (Dijon, Bourgogne-Franche-Comté) a été ajoutée le 20/11 à partir de son site officiel ; deux adresses différentes figurent sur ses pages et restent à confirmer. Voir [les sources et réserves](premiers-prospects.md) le [contrôle de prospection du 19 novembre](controle-prospection-19-nov-2026.md) et le [contrôle de prospection du 20 novembre](controle-prospection-20-nov-2026.md). Une piste AÏDIYO (Guadeloupe) a été ajoutée le 21/11 à partir des mentions légales, de la page Contact et de l’accueil officiels ; les prestations d’entretien préventif pour professionnels sont publiées, mais aucun besoin de tableur n’est confirmé. Le 22/11, trois pistes ont été ajoutées à partir de sites officiels : E.T.C Normandie (Normandie, téléphone public sans e-mail direct relevé), Occitanie Sports Loisirs (Occitanie, e-mail et téléphone publics) et Winovatio (PACA, e-mail et téléphone publics). Leurs activités de maintenance sont publiées, mais aucun besoin de tableur n’est confirmé. Le 23/11, quatre pistes existantes (AÏDIYO en Guadeloupe, E.T.C Normandie, Occitanie Sports Loisirs et Winovatio) ont été revalidées sur leurs pages officielles : coordonnées générales et activités publiées confirmées, aucun besoin de tableur confirmé, aucun contact effectué. Le 24/11, Liagre Plomberie (Hauts-de-France) et S.M.T — Salazienne de Maintenances et Techniques (La Réunion) ont été ajoutées après consultation de leurs sites officiels ; coordonnées professionnelles publiées, besoin de tableur inconnu, aucun contact effectué. Pour Winovatio, contact@winovatio.fr figure sur l’accueil et dg@winovatio.com dans les mentions légales ; pour E.T.C Normandie, aucun e-mail direct n’a été relevé sur la page Contact. Le 26/11, Le Breton - Basselot (Bretagne) et CPC Services (Centre-Val de Loire) ont été ajoutées depuis leurs pages Professionnel/Contact officielles : e-mails et téléphones publiés, activité décrite, besoin de tableur inconnu et aucun contact effectué. Le contrôle du 17/11 est structurel et ne revalide pas individuellement chaque coordonnée. Avant toute démarche, vérifier à nouveau la page officielle, le rôle du destinataire, le canal approprié et toute opposition. Ne jamais utiliser un numéro d'urgence ou de dépannage comme canal commercial.

- [Liste nationale des prospects et sources](premiers-prospects.md)
- [Contrôle de prospection du 20 novembre](controle-prospection-20-nov-2026.md)
- [Contrôle des impressions du 21 novembre](controle-impression-classeurs-21-nov-2026.md)
- [Contrôle du site public du 21 novembre](controle-site-21-nov-2026.md)
- [Contrôle de prospection du 21 novembre](controle-prospection-21-nov-2026.md)
- [Contrôle de prospection du 22 novembre](controle-prospection-22-nov-2026.md)
- [Contrôle du site du 22 novembre](controle-site-22-nov-2026.md)
- [Contrôle de l'exemple Tableau simple du 22 novembre](controle-tableau-simple-22-nov-2026.md)
- [Contrôle de prospection du 24 novembre](controle-prospection-24-nov-2026.md)
- [Contrôle partiel du Tableau simple du 24 novembre](controle-tableau-simple-24-nov-2026.md)
- [Correction de la zone d'impression du Tableau simple v1.1 — 25 novembre](controle-tableau-simple-25-nov-2026.md)
- [Contrôle de clarté du site public — 25 novembre](controle-site-25-nov-2026.md)
- [Contrôle de prospection du 26 novembre](controle-prospection-26-nov-2026.md)
- [Guide de recette externe du Tableau simple](guide-recette-externe-tableau-simple.md)
- [Plan de recette du Tableau simple](plan-recette-acceptation-ods.md)
- [Contrôle du site du 24 novembre](controle-site-24-nov-2026.md)
- [Contrôle et publication de l'aperçu Tableau simple du 23 novembre](controle-exemple-public-23-nov-2026.md)
- [Aperçu PDF du suivi des demandes](exemples/suivi-demandes-apercu.pdf)
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

Le 22/11/2026, un exemple local de l'offre « Tableau simple » a été créé en démonstration et en version vierge : suivi de demandes sur 50 lignes, listes de priorité/statut, filtres et guide. Les propriétés de validation ont été inspectées via LibreOffice Calc ; le test visuel au clic, Excel et la personnalisation à partir d'un besoin réel restent à faire. Les classeurs ODS ne sont pas publiés dans le dépôt. Le 23/11/2026, un aperçu PDF de présentation d'une page A4 paysage a été créé à partir des six lignes fictives du classeur puis publié dans `exemples/suivi-demandes-apercu.pdf`. Il montre les champs, listes, filtres et limites de l'offre ; il ne remplace pas le classeur ODS et ne constitue pas une validation interactive. Le 24/11/2026, le Tableau simple (démonstration et version vierge) a été ouvert, sauvegardé sur copie puis rouvert avec LibreOffice Calc 25.2.3.2 via UNO : feuilles présentes, 50 lignes prévues, six demandes fictives dans la démonstration et aucune dans la version vierge, validations Priorité/Statut présentes sur la première et dernière ligne et conservées après réouverture, validation conservée après copie temporaire. Les PDF exportés depuis Calc ont été inspectés (2 pages pour la démonstration, 3 pour la version vierge). La plage de filtre est déclarée dans le XML ODS, mais les menus n'ont pas été testés au clic. Les saisies interdites, le tri, le copier-coller manuel, le test extérieur, Excel et l'impression physique restent à faire ; le produit n'est pas déclaré prêt à la vente. Voir le [contrôle partiel du 24 novembre](controle-tableau-simple-24-nov-2026.md).

## Points bloquants

- Les tests interactifs dans l'interface de LibreOffice Calc et un test utilisateur extérieur restent à faire.
- Excel n'a pas été testé.
- Les doublons sont détectés, mais pas bloqués.
- Les mentions légales et la politique de confidentialité ne sont pas publiées : les informations exactes de l'exploitant et les vérifications nécessaires manquent. Ne pas inventer ni publier de coordonnées juridiques.
- Les binaires ODS ne sont pas publiés dans le dépôt public. Seul le catalogue PDF informatif est publié.

## Garde-fous

- Aucun e-mail commercial, appel ou formulaire envoyé.
- Aucune dépense engagée.
- Aucun engagement juridique pris.
- Les exemples de tableurs sont fictifs.
- Aucun besoin de prospect n'est présenté comme confirmé sans preuve.


Le 25/11/2026, la recette PDF du Tableau simple a révélé que la version vierge n'imprimait que 20 des 50 lignes prévues. La plage d'impression a été corrigée sur une copie en A1:I54 ; les deux exports ont été régénérés. Le PDF vierge comporte toujours trois pages au total : une page de guide puis deux pages de tableau, chacune présentant 25 lignes. Les deux ODS conservent 100 cellules validées, deux règles de validation et une plage de filtre déclarée. Les interactions à la souris et les autres essais listés dans le plan de recette restent non exécutés. Voir le [rapport du 25 novembre](controle-tableau-simple-25-nov-2026.md).
