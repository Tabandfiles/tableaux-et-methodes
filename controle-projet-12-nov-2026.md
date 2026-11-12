# Contrôle du projet — 12 novembre 2026

## Dépôt et site

- Dépôt : [Tabandfiles/tableaux-et-methodes](https://github.com/Tabandfiles/tableaux-et-methodes), branche `main`.
- Au contrôle initial de cette journée, le commit de tête était `08bf66bd4ff1cea40dc44331c52e96ede7fa55ef` et l'arborescence contenait 19 fichiers.
- Aucun fichier binaire `.ods` ou `.xlsx` n'était présent dans l'arborescence publique.
- Le dernier workflow Pages visible est le n° 75, terminé avec succès le 11 novembre 2026 : [historique des workflows](https://github.com/Tabandfiles/tableaux-et-methodes/actions).
- Le site public a été relu le 12 novembre : [Tableaux & Méthodes](https://tabandfiles.github.io/tableaux-et-methodes/). Le suivi de stock y est correctement annoncé comme en préparation et indisponible à la livraison.

## Améliorations réalisées dans ce commit de travail

- Les offres sont présentées comme des créations à la demande et non comme un catalogue de fichiers prêts à télécharger.
- Les appels à l'action des cartes ont été reformulés en « Décrire mon besoin ».
- La liste de prospection et son CSV ont été étendus à cinq pistes ultramarines, chacune avec des sources officielles.
- Le README, la fiche produit, la spécification et le journal de tests distinguent maintenant les résultats historiques rapportés pour l'ODS v2.1 de la disponibilité actuelle du binaire.

## Cinq pistes ultramarines vérifiées le 12 novembre

| Territoire | Entreprise | Coordonnées officielles | Sources |
|---|---|---|---|
| Guadeloupe | Société de Maintenance Industrielle | 09 74 56 40 64 ; formulaire ; aucun e-mail direct relevé | [Accueil](https://www.smi-guadeloupe.fr/) · [Contact](https://www.smi-guadeloupe.fr/contactez-nous.php) |
| Martinique | Clean Plomberie | yannick@cleanplomberie.com · +596 696 00 41 21 | [Site officiel](https://cleanplomberie.com/) |
| La Réunion | Climatech | climatech.reunion@gmail.com · 06 92 86 49 05 · 02 62 46 61 45 | [Service entretien](https://climatech974.com/services/entretien) |
| Guyane | MI&HG | contact@mihg.fr ; formulaire | [Contact](https://www.mihg.fr/contact/) |
| Mayotte | Actemium Maintenance Océan Indien | +33 2 69 63 71 12 · ludovic.pierne@actemium.com (contact partagé) | [Présentation](https://www.actemium.fr/implantations/actemium-mayotte/presentation/) · [Contact](https://www.actemium.fr/implantations/actemium-mayotte/contact/) |

Les cinq entreprises restent des pistes non qualifiées. La présence d'un planning de chantier, d'une activité de maintenance ou d'un formulaire public ne prouve pas un besoin de tableur. Aucun e-mail, appel ou formulaire n'a été envoyé.

## État des produits

- **Suivi de stock :** le journal v2.1 du 9 novembre rapporte des tests Calc réussis, mais le binaire ODS n'est pas présent dans le dépôt public ni dans les fichiers accessibles lors de ce contrôle. La v1 jointe précédemment reste une maquette à cumuls manuels et ne doit pas être livrée comme stock automatisé.
- **Suivi de maintenance :** spécification uniquement ; aucun ODS final créé.
- **Registre d'interventions :** spécification uniquement ; aucun ODS final créé.
- **Tableau simple :** offre de création à la demande ; aucun modèle binaire vérifié dans le dépôt.

## Blocages et précautions

- Le classeur ODS v2.1 doit être récupéré ou reconstruit, puis ouvert, recalculé et testé dans LibreOffice Calc avant toute livraison.
- Les mentions légales et la politique de confidentialité sont des brouillons incomplets : les informations exactes de l'exploitant manquent.
- Aucune compatibilité Excel n'est promise.
- Aucun message commercial n'a été envoyé, aucune dépense engagée et aucun engagement juridique pris.

## Prochaine priorité

Récupérer le binaire v2.1 s'il existe dans un espace de travail antérieur accessible ; sinon reconstruire le classeur de stock et revalider les calculs, les filtres et les validations de saisie dans LibreOffice Calc. Ne publier le produit comme disponible qu'après ces contrôles.


## Vérification finale après publication

- Le workflow Pages n° 83 a terminé avec succès le 12 novembre 2026 : [run n° 83](https://github.com/Tabandfiles/tableaux-et-methodes/actions/runs/43280484994).
- Une nouvelle lecture du site public confirme les six CTA « Décrire mon besoin » et le texte précisant que les offres sont des créations à la demande, pas des téléchargements immédiats.
- Le workflow n° 84, déclenché par la correction du CSV, s'est terminé avec succès. Le workflow n° 86, déclenché par les dernières mises à jour documentaires, a également terminé ses trois étapes build, report-build-status et deploy avec succès : [run n° 86](https://github.com/Tabandfiles/tableaux-et-methodes/actions/runs/43280829621).
- Le CSV final a été relu : 23 entreprises, 17 colonnes pour chacune des 23 lignes, aucun doublon et cinq nouvelles pistes DROM présentes. Les deux lignes historiques contenant des séparateurs non conformes ont également été corrigées.
- Aucun fichier ODS ou XLSX n'a été ajouté : le blocage du binaire v2.1 demeure.
