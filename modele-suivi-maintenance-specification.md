# Cahier des charges — Suivi de maintenance

**Produit :** Suivi de maintenance simple  
**Prix de lancement envisagé :** 25 €  
**Format cible :** LibreOffice Calc (.ods)  
**Statut au 6 novembre 2026 :** spécification écrite ; aucun fichier ODS final créé pour ce produit. Les formules ci-dessous sont des références de conception, non testées dans un classeur.

## Objectif et périmètre

Aider une petite entreprise, un artisan ou une association à repérer les équipements à entretenir et à conserver un historique simple. Le modèle ne doit pas se présenter comme une GMAO, un outil de conformité ou un système d'alerte automatique.

## Feuille 1 — « Équipements »

Une ligne par équipement :

| Colonne | Champ | Règle |
|---|---|---|
| A | Référence | Identifiant unique, par exemple EQ-001 |
| B | Équipement | Nom compréhensible |
| C | Site / emplacement | Lieu ou zone |
| D | Catégorie | Famille d'équipement |
| E | Opération prévue | Contrôle, nettoyage, remplacement, etc. |
| F | Périodicité (jours) | Nombre entier positif |
| G | Dernière intervention | Date connue ; saisie manuelle en version 1 |
| H | Prochaine échéance | Calculée si la périodicité et la dernière date sont renseignées |
| I | Jours restants | Différence entre l'échéance et la date du jour |
| J | État calculé | À planifier, En retard, À prévoir ou Planifié |
| K | Responsable | Facultatif |
| L | Commentaires | Facultatif |

### Formules de référence (non testées)

Pour la ligne 2, avec une interface française de Calc et des séparateurs « ; » :

- **Prochaine échéance (H2)** : `=SI(OU(A2="";F2="";G2="");"";G2+F2)`
- **Jours restants (I2)** : `=SI(H2="";"";H2-AUJOURDHUI())`
- **État calculé (J2)** : `=SI(A2="";"";SI(H2="";"À planifier";SI(H2<AUJOURDHUI();"En retard";SI(H2<=AUJOURDHUI()+7;"À prévoir";"Planifié"))))`

Ces formules doivent être testées dans LibreOffice Calc avant d'être intégrées à un fichier livré. Prévoir un traitement explicite des équipements retirés du service si cette fonction est ajoutée.

## Feuille 2 — « Historique »

Une ligne par opération réellement effectuée :

| Colonne | Champ | Utilisation |
|---|---|---|
| A | Date | Date de réalisation |
| B | Référence équipement | Doit correspondre à une référence de la feuille Équipements |
| C | Opération réalisée | Action effectuée |
| D | Type | Préventive, corrective, contrôle, autre |
| E | Intervenant | Personne ou équipe |
| F | Durée (h) | Nombre positif ou nul |
| G | Résultat / compte rendu | Observations utiles |
| H | Suite à donner | Pièce, devis, contrôle, prochaine visite |
| I | Commentaires | Facultatif |

**Limite de la version 1 :** l'historique ne met pas automatiquement à jour la date de dernière intervention dans « Équipements ». L'utilisateur la met à jour manuellement après l'opération. Ne pas annoncer une synchronisation automatique tant qu'elle n'est pas construite et testée.

## Feuille 3 — « Tableau de bord »

Indicateurs proposés :
- Nombre d'équipements renseignés ;
- échéances en retard ;
- échéances à prévoir dans les 7 jours ;
- équipements à planifier ;
- opérations inscrites dans l'historique.

Les indicateurs doivent ignorer les lignes vides. Les formules de comptage seront choisies et testées avec la version cible de Calc.

## Feuille 4 — « Guide »

1. Créer une référence unique par équipement.
2. Saisir l'opération prévue et la périodicité en jours.
3. Saisir la date de dernière intervention si elle est connue.
4. Contrôler les échéances calculées et corriger les données erronées.
5. Après chaque opération, ajouter une ligne dans « Historique ».
6. Mettre à jour manuellement la dernière date dans « Équipements ».
7. Filtrer les états « En retard », « À prévoir » et « À planifier ».
8. Faire des sauvegardes régulières et limiter les informations personnelles au nécessaire.

## Ergonomie et livraison

- Filtres activés et ligne d'en-tête figée.
- Dates au format JJ/MM/AAAA ; durées en heures.
- Alerte textuelle accompagnant toute couleur.
- Listes modifiables pour les catégories et types d'opération, si les validations sont testées.
- Données d'exemple exclusivement fictives.
- Aucune macro obligatoire.
- Une notice courte expliquant les cellules à modifier et les limites.

## Tests avant commercialisation

- Équipement sans dernière date ;
- échéance hier, aujourd'hui, dans 7 jours et dans 8 jours ;
- périodicité vide, nulle et négative ;
- ligne d'équipement vide ;
- plusieurs historiques pour la même référence ;
- référence inconnue dans l'historique ;
- tri et filtres sans décalage des lignes ;
- ouverture, enregistrement et réouverture dans LibreOffice Calc ;
- compatibilité Excel testée séparément si elle est annoncée.

## Hors périmètre

Pas de notification par e-mail, de calendrier partagé, de connexion à un logiciel métier, de gestion de pièces, de facturation ni de garantie de conformité réglementaire. Les données et échéances doivent être vérifiées par l'utilisateur.

## Prochaine étape

Construire le fichier ODS, tester les formules et les cas limites, puis produire un aperçu fictif. Le modèle ne doit être présenté comme prêt à vendre qu'après validation de la grille de contrôle qualité.
