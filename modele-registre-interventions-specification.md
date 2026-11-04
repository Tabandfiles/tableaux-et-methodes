# Cahier des charges — Registre de suivi des interventions

**Produit :** Registre des interventions  
**Prix de lancement envisagé :** 25 €  
**Format cible :** LibreOffice Calc (.ods)  
**Statut :** spécification préparée ; fichier téléchargeable non créé et formules non testées.

## Objectif

Permettre à un artisan, une petite entreprise de maintenance ou une association de consigner les demandes et interventions, de suivre leur état et de retrouver rapidement l'historique. Le modèle doit rester simple, utilisable sans logiciel métier ni abonnement.

## Structure du classeur

### Feuille 1 — « Interventions »

Une ligne par intervention.

| Colonne | Nom | Utilisation |
|---|---|---|
| A | N° intervention | Identifiant unique, par exemple INT-0001 |
| B | Date de demande | Date de réception de la demande |
| C | Client / site | Nom du client ou lieu concerné |
| D | Contact | Nom ou service du demandeur, facultatif |
| E | Téléphone / e-mail | Coordonnée utile, facultative |
| F | Équipement / zone | Matériel ou emplacement concerné |
| G | Description | Motif et symptômes signalés |
| H | Priorité | Basse, normale, haute, urgente |
| I | Technicien | Personne affectée |
| J | Date prévue | Date planifiée |
| K | Date réalisée | Date effective |
| L | Statut | À planifier, planifiée, en cours, en attente, terminée, annulée |
| M | Durée (h) | Temps passé, en heures |
| N | Compte rendu | Travail effectué et constat |
| O | Suite à donner | Pièce à commander, devis, contrôle, nouvelle visite |
| P | Date de clôture | Date de clôture administrative |
| Q | Commentaires | Informations complémentaires |

### Feuille 2 — « Listes »

Valeurs de référence pour les listes déroulantes :
- Priorité : Basse ; Normale ; Haute ; Urgente.
- Statut : À planifier ; Planifiée ; En cours ; En attente ; Terminée ; Annulée.
- Type de demande : Préventive ; Corrective ; Contrôle ; Autre.

Les listes doivent être modifiables par l'utilisateur et clairement identifiées.

### Feuille 3 — « Tableau de bord »

Indicateurs simples calculés à partir de la feuille Interventions :
- Nombre total d'interventions enregistrées.
- Nombre d'interventions à planifier.
- Nombre d'interventions planifiées.
- Nombre d'interventions en cours.
- Nombre d'interventions en attente.
- Nombre d'interventions terminées.
- Nombre d'interventions urgentes non terminées.

Ajouter un filtre par période si cela peut être fait sans macro. Les indicateurs doivent exclure les lignes vides.

### Feuille 4 — « Guide »

1. Créer un numéro unique pour chaque nouvelle demande.
2. Saisir la date de demande, le client/site et la description.
3. Choisir une priorité et un statut.
4. Renseigner le technicien et la date prévue si connus.
5. Mettre à jour le statut au fil de l'intervention.
6. Compléter la date réalisée, la durée et le compte rendu.
7. Indiquer les suites à donner avant de clôturer.
8. Utiliser les filtres pour retrouver une intervention.
9. Effectuer des sauvegardes régulières.

## Présentation et ergonomie

- En-têtes figés et filtres activés.
- Largeurs adaptées, retour à la ligne pour les descriptions et comptes rendus.
- Dates au format JJ/MM/AAAA.
- Durées en heures avec une décimale au maximum.
- Mise en évidence des priorités urgentes et des interventions en attente.
- Lignes d'exemple fictives, clairement signalées comme exemples.
- Aucun renseignement réel de client dans la démonstration.
- Aucune macro obligatoire ; compatibilité LibreOffice Calc prioritaire.

## Limites à afficher clairement

- Ce registre n'est pas une GMAO et ne remplace pas un logiciel réglementaire ou métier.
- Il ne gère pas automatiquement les plannings, les notifications, les stocks de pièces ou la facturation.
- Les données personnelles saisies doivent être limitées au nécessaire et protégées par l'utilisateur.
- L'utilisateur reste responsable de ses sauvegardes et de la gestion des accès au fichier.

## Tests avant commercialisation

1. Ajouter plusieurs interventions avec des statuts et priorités différents.
2. Vérifier que les indicateurs ne comptent pas les lignes vides.
3. Vérifier les filtres par statut, priorité, technicien et date.
4. Tester les listes déroulantes et leur modification.
5. Vérifier le tri sans dissocier les données des lignes.
6. Enregistrer, fermer et rouvrir dans LibreOffice Calc.
7. Tester les cellules vides, dates invalides et durées négatives.
8. Vérifier l'impression et la lisibilité sur écran d'ordinateur.
9. Vérifier qu'aucune formule ne se casse lors de l'ajout de lignes.

## À faire ensuite

1. Construire le fichier .ods.
2. Tester toutes les formules et listes dans LibreOffice Calc.
3. Créer un aperçu avec données fictives.
4. Ajouter le produit au site seulement lorsque le fichier est réellement prêt.
5. Définir précisément ce qui est inclus dans le prix de lancement de 25 €.
