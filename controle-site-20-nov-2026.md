# Contrôle du site et cohérence des exemples — 20 novembre 2026

## Dépôt

- Dépôt public : https://github.com/Tabandfiles/tableaux-et-methodes
- Branche par défaut : main
- Le dépôt est public, non archivé ; les permissions du connecteur autorisent la lecture et l'écriture.
- Le dernier commit contrôlé est `2801ab3b72e2fa107df7840e6d056076b568bd52` ; le workflow GitHub Pages n°44792786546 a terminé avec succès (build, deploy et rapport de statut).

## Site public consulté

- Accueil : https://tabandfiles.github.io/tableaux-et-methodes/
- Catalogue : https://tabandfiles.github.io/tableaux-et-methodes/catalogue.pdf
- Sitemap : https://tabandfiles.github.io/tableaux-et-methodes/sitemap.xml
- Robots : https://tabandfiles.github.io/tableaux-et-methodes/robots.txt

L'accueil et le catalogue sont accessibles. Le sitemap contient l'unique page HTML du site, ce qui correspond à la structure monopage actuelle. Le catalogue PDF du 19/11/2026 est accessible publiquement.

## Incohérence détectée et corrigée

Le texte de la carte « Suivi de maintenance » disait encore que la dernière date préventive devait être mise à jour manuellement, alors que le classeur v1.1 et le catalogue PDF décrivaient déjà une synchronisation depuis le journal.

La carte a été corrigée le 20/11/2026. Elle précise maintenant les conditions exactes du calcul : même identifiant d'équipement, type « Préventive » et résultat « Réalisée ». Elle rappelle que le classeur n'est pas une GMAO et reste non disponible à la livraison tant que la recette visuelle et utilisateur n'est pas terminée.

La démonstration ODS présentait une seconde incohérence : VAN-003 affichait une préventive au 10/11/2026 sur le site, mais son journal contenait un « Contrôle » au 12/11/2026. Le journal de la démonstration a été corrigé pour enregistrer une préventive réalisée le 10/11/2026. Les indicateurs du tableau de bord correspondent alors aux valeurs annoncées : 3 équipements, 1 en retard, 1 à planifier sous 30 jours, 1 à jour, 4 interventions et 5 heures.

## Prospection nationale — contrôle structurel du CSV

Contrôle du fichier `suivi-prospection.csv` :
- 33 lignes de données et 33 entreprises distinctes.
- 17 colonnes.
- 18 territoires libellés : 13 régions métropolitaines et 5 DROM.
- 21 lignes avec e-mail public et 31 lignes avec téléphone public.
- Une URL de source par ligne.
- Aucun doublon.
- Aucun besoin marqué confirmé.
- Aucun contact marqué effectué.

Ce contrôle est structurel et ne constitue pas une revalidation individuelle en direct des 33 coordonnées. Les sources officielles doivent être relues avant toute démarche.

## Limites et garde-fous

Les tests de calcul via LibreOffice Calc UNO ne remplacent pas les tests visuels au clavier et à la souris, les essais de filtres, de validation, de copier-coller, d'impression, la compatibilité Excel ou un test utilisateur extérieur. Les trois familles de prototypes restent non disponibles à la livraison.

Aucun e-mail commercial n'a été envoyé, aucun appel passé, aucun formulaire soumis, aucune dépense engagée et aucun engagement juridique pris. Les mentions légales restent à compléter uniquement à partir des informations exactes de l'exploitant.
