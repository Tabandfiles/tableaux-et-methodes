# Contrôle du site public — 11 novembre 2026

## Périmètre vérifié

- Dépôt : `Tabandfiles/tableaux-et-methodes`
- Branche : `main`
- Site : https://tabandfiles.github.io/tableaux-et-methodes/
- Contrôle du dépôt : API GitHub, arborescence racine, contenu de `index.html`, `README.md`, fiche produit et grille qualité.
- Contrôle du site : extraction de la page publique et de ses métadonnées.

## État du dépôt

Le dépôt est public, non archivé et la branche par défaut est `main`. La racine contient les documents de cadrage, la prospection, les spécifications et le site. Aucun binaire ODS v2.1 n'est présent à la racine ; le fichier n'est pas publié dans le dépôt.

Le commit de clarification du site est :

- SHA : `519bf4cb8c4625b2ed9367c799179d5f6df4577a`
- Fichier modifié : `index.html`
- Objet : ne plus présenter le suivi de stock automatisé comme disponible alors que le binaire final n'est pas récupérable pour contrôle.

## Correction apportée à la page

La fiche « Suivi de stock » et la réponse FAQ sur sa capacité indiquent désormais que :

- le modèle automatisé est en préparation et n'est pas encore disponible à la livraison ;
- 100 références et 500 mouvements sont une cible de conception, pas une capacité actuellement garantie ;
- le calcul automatique et les alertes ne seront annoncés comme disponibles qu'après contrôle du fichier final dans LibreOffice Calc ;
- la disponibilité, le périmètre et le prix seront confirmés avant toute commande.

Cette correction évite de transformer le journal de tests documentaire de la v2.1 en preuve de disponibilité d'un fichier binaire qui n'a pas pu être ouvert lors des contrôles précédents.

## État du déploiement au moment du contrôle

- Dernier déploiement confirmé avant la correction : workflow Pages n° 42877381234, terminé avec succès le 10 novembre 2026.
- Le workflow n° 43076148310 (commit de correction HTML) a été annulé après des commits plus récents. Le workflow n° 43076201925 (rapport) a également été annulé. Les workflows n° 43076218312 puis 43076301547 étaient en attente lors du dernier contrôle, le second correspondant à la mise à jour de la prospection.
- La dernière extraction publique effectuée avant la fin de ces workflows renvoyait encore l'ancien texte. Il ne faut donc pas déclarer la correction publiée tant qu'un workflow pour le dernier commit n'est pas terminé et que la page en ligne n'a pas été relue.

## Revalidation de prospection — 11 novembre 2026

Trois sites officiels ont été relus : A2L Chauffage Plomberie (Normandie), SBE (Bourgogne-Franche-Comté) et CMH Industrie (Provence-Alpes-Côte d’Azur). Les informations confirmées et les réserves sont consignées dans [la liste nationale des prospects](premiers-prospects.md). Aucun contact n'a été envoyé.

## État commercial et limites

- Le suivi de stock automatisé ne doit pas être vendu ou remis comme produit prêt tant que le fichier final n'est pas récupéré ou reconstruit et contrôlé.
- Le prototype v1 reste une maquette à cumuls manuels ; il ne calcule pas les entrées/sorties à partir du journal.
- Les filtres, validations de saisie et l'ergonomie doivent encore être vérifiés dans Calc.
- Les mentions légales et la confidentialité restent à compléter avec les informations exactes de l'exploitant.
- Les 18 pistes de prospection documentées restent non qualifiées ; aucune coordonnée n'a été revalidée dans ce contrôle.
- Aucun e-mail commercial envoyé, aucune dépense engagée, aucun engagement juridique pris.

## Prochaine action

Attendre la fin du workflow 43076148310, relire le site public, puis seulement après cette vérification marquer la correction comme publiée. La priorité produit reste la récupération ou la reconstruction contrôlable du fichier ODS automatisé.
