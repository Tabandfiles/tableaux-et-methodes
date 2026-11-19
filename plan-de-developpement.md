# Plan d'avancement — Tableaux & Méthodes

Ce document fixe les prochaines étapes du projet sans supposer de budget publicitaire ni d'abonnement payant. L'objectif commercial de 500 €/mois est une cible à tester, pas une garantie de revenus.

## Priorités immédiates

### 1. Rendre les offres simples à acheter
- Garder les offres de base lisibles : tableau simple (15 €), stock (20 €), maintenance (25 €), interventions (25 €), tableau de bord (dès 40 €).
- Avant chaque réalisation, confirmer par écrit le contenu, le format, le délai, le prix et ce qui est inclus.
- Ne pas promettre une automatisation complexe au prix d'un tableau simple.
- Proposer en priorité LibreOffice Calc et vérifier la compatibilité Excel selon les fonctions utilisées.

### 2. Créer trois produits réutilisables
1. **Suivi de stock** : articles, références, quantités, seuil d'alerte, mouvements, fournisseur et date de mise à jour.
2. **Suivi de maintenance** : équipement, emplacement, opération, dernière intervention, périodicité, prochaine échéance, statut.
3. **Registre d'interventions** : date, demande, priorité, responsable, action réalisée, statut, date de clôture et commentaires.

Chaque modèle doit être testé avec des données fictives, des instructions claires et des colonnes faciles à personnaliser. Ne pas y inclure de données clients réelles.

### 3. Développer la prospection nationale
- Viser d'abord artisans et petites entreprises techniques, puis associations sportives.
- Chercher des prospects dans toutes les régions, sans faire dépendre les ventes d'une seule zone.
- Qualifier 10 à 20 structures à la fois ; vérifier l'activité et le contact sur le site officiel.
- Personnaliser chaque message. Aucun envoi automatique ni campagne massive.
- Enregistrer les réponses et oppositions dans le fichier de suivi.

### 4. Améliorer la crédibilité du site
- Conserver les exemples explicitement marqués comme fictifs.
- Afficher les prix de départ et rappeler qu'un périmètre est confirmé avant réalisation.
- Vérifier régulièrement les liens de contact et le rendu mobile.
- Ne pas ajouter de témoignages ou de logos clients inventés.
- Ajouter des exemples téléchargeables seulement après avoir créé et testé de vrais fichiers de démonstration.

## Plan de test commercial sur 4 semaines

### Semaine 1 — Préparation
- Vérifier le site et les liens e-mail.
- Finaliser le modèle de suivi de stock et un exemple fictif.
- Préparer un message d'approche court par secteur.

### Semaine 2 — Première validation
- Constituer une petite liste nationale de prospects vérifiés.
- Contacter manuellement quelques structures adaptées, après contrôle de la conformité et personnalisation.
- Noter les réponses et les objections ; ne pas interpréter le silence comme une validation du produit.

### Semaine 3 — Ajustements
- Adapter les descriptions des offres aux questions reçues.
- Créer le second modèle le plus demandé.
- Vérifier si les prix couvrent réellement le temps de conception et de correction.

### Semaine 4 — Décision
- Comparer les demandes reçues, les réponses et le temps consacré.
- Conserver les offres qui suscitent un intérêt réel ; simplifier ou abandonner celles qui n'en suscitent pas.
- Revoir les tarifs si les demandes dépassent le périmètre annoncé.

## Mesures simples à suivre

- Nombre de prospects qualifiés ;
- nombre de messages personnalisés envoyés ;
- réponses positives, refus et oppositions ;
- demandes de devis ;
- ventes réellement conclues ;
- temps passé par fichier ;
- corrections demandées après livraison ;
- revenu encaissé, séparé du chiffre d'affaires espéré.

## Garde-fous

- Aucun achat d'outil ou abonnement sans accord explicite.
- Aucun message envoyé automatiquement.
- Aucune affirmation sur les économies ou les résultats clients sans preuve.
- Vérifier les règles fiscales, administratives et les éventuelles obligations liées à l'activité avant les premières ventes.
- Les données d'entreprises et les adresses de contact doivent provenir de sources publiques et être utilisées de façon proportionnée.

## Liens utiles

- Site : https://tabandfiles.github.io/tableaux-et-methodes/
- Liste de prospects : https://github.com/Tabandfiles/tableaux-et-methodes/blob/main/premiers-prospects.md
- Suivi commercial : https://github.com/Tabandfiles/tableaux-et-methodes/blob/main/suivi-prospection.csv
- Annuaire officiel des entreprises : https://annuaire-entreprises.data.gouv.fr/
- Contact : tabsandmethod@gmail.com


## Point d'avancement — 15 novembre 2026

- Suivi de stock : prototype local v2.2, démonstration et version vierge ; 507 formules par fichier ; signalement des références dupliquées ; scénarios de calcul et doublons recalculés dans LibreOffice. Toujours en préparation tant que les interactions au clic et le test utilisateur ne sont pas validés.
- Registre d'interventions : prototype local v1.0, démonstration et version vierge ; quatre feuilles, 200 lignes prévues, 210 formules, cinq règles de validation et filtre. Les indicateurs, doublons et frontière de capacité ont été testés dans LibreOffice.
- Suivi de maintenance : cahier des charges seulement ; aucun ODS créé à cette date.
- Site : ajout d'un lien d'évitement, prise en compte de la préférence de réduction des animations et harmonisation des métadonnées de partage. Publication vérifiée : workflow Pages n° 43746840172 terminé avec succès le 15/11/2026 ; métadonnées publiques relues après déploiement.
- Prospection : 27 pistes sur 18 territoires ; cinq coordonnées officielles revalidées le 15/11/2026. Aucun besoin confirmé et aucun contact effectué.

### Priorités suivantes
1. Faire un essai graphique au clic des listes et filtres des deux prototypes dans LibreOffice Calc.
2. Faire tester le registre et le stock par une personne non technique ; corriger les points de friction.
3. Construire le suivi de maintenance ODS à partir du cahier des charges.
4. Revalider les autres coordonnées nationales au fil de l'eau, sans augmenter artificiellement le nombre de pistes.
5. Ne modifier le statut public des offres qu'après validation des livrables.


Complément du 15/11/2026 : la validation de date a été ajoutée au registre d'interventions (type DATE, bornes 1900–9999, alerte STOP) et relue dans LibreOffice via UNO.


## Mise à jour du 19 novembre 2026

- Le suivi de maintenance passe en prototype v1.1 : la dernière préventive réalisée est calculée depuis le journal des interventions ; les correctives et les préventives non réalisées ne repoussent pas l'échéance.
- Tests Calc via UNO sur copies temporaires : mouvements et alertes du stock, compteurs du registre, doublons, filtres, validations et mise à jour automatique de maintenance vérifiés.
- Les tests visuels au clic, les impressions, la compatibilité Excel et un test utilisateur extérieur restent à réaliser avant toute mise en vente.
- Le catalogue PDF informatif est publié sur le site ; il ne présente pas les prototypes comme disponibles.
- Prospection nationale : 33 pistes dans 18 territoires ; les deux nouvelles pistes du 19/11 ont des coordonnées publiques officielles, mais aucun besoin confirmé et aucun contact effectué.
- Prochaine priorité : recette visuelle dans Calc, puis contrôle d'impression et test utilisateur indépendant.
