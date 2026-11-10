# Inventaire des tableurs déjà présents dans la bibliothèque — 10 novembre 2026

## Objet et méthode

Recherche dans les fichiers de la bibliothèque et inspection en lecture seule de deux classeurs Excel retrouvés. Cet inventaire distingue les fichiers réellement présents des modèles ODS décrits dans les documents du dépôt. Il ne vaut pas validation commerciale ni validation LibreOffice.

## 1. Pack multi-suivi

**Fichier retrouvé :** `pack_modeles_suivi_numerique.xlsx`  
**Taille :** 15 228 octets  
**Format :** XLSX  
**Feuilles :** Résumé, Maintenance, Stock, Interventions, Mode d'emploi.

### Contenu réellement observé

- **Maintenance :** 50 formules sur 25 lignes prévues (prochaine échéance et statut calculés à partir de la dernière date et de la périodicité). Validation de données sur la périodicité : nombre entier supérieur ou égal à 1.
- **Stock :** 50 formules sur 25 lignes (indicateur de commande selon le seuil et valeur indicative du stock). Validation de données sur le prix unitaire : nombre décimal supérieur ou égal à 0.
- **Interventions :** données structurées et validations de listes pour la priorité et le statut ; aucune formule de calcul observée dans cette feuille.
- **Résumé :** 5 indicateurs calculés à partir des trois feuilles.
- Des tableaux structurés Excel sont présents dans les trois feuilles opérationnelles.

### Limites observées

- Le stock repose sur une quantité actuelle saisie directement : il n'y a pas de journal d'entrées/sorties qui recalcule le stock.
- La feuille Interventions ne calcule pas de tableau de bord détaillé par statut dans sa propre feuille ; le résumé compte les interventions ouvertes.
- Les résultats recalculés des formules ne sont pas enregistrés dans le cache du fichier. Le recalcul et le rendu doivent être vérifiés dans LibreOffice Calc.
- Le fichier est un XLSX, pas un ODS. Aucune compatibilité LibreOffice ne doit être annoncée avant un test réel.

## 2. Modèle de maintenance autonome

**Fichier retrouvé :** `modele_suivi_maintenance_demo.xlsx`  
**Taille :** 10 235 octets  
**Format :** XLSX  
**Feuilles :** Suivi équipements, Résumé, Mode d'emploi.

### Contenu réellement observé

- 48 formules sur 24 lignes prévues : prochaine date calculée et statut selon la date du jour.
- 4 formules de synthèse : équipements renseignés, contrôles en retard, contrôles sous 7 jours et contrôles à jour.
- Validation de données sur la périodicité : nombre entier supérieur ou égal à 1.
- Un tableau structuré est présent dans la feuille opérationnelle.

### Limites observées

- La dernière intervention est saisie manuellement ; aucun historique séparé ne met automatiquement à jour cette date.
- Les résultats recalculés des formules ne sont pas enregistrés dans le cache du fichier.
- Le fichier est un XLSX, pas un ODS. Aucun test de recalcul ou de rendu dans LibreOffice Calc n'a été effectué pendant cet inventaire.

## 3. Différence avec le suivi de stock ODS v2.1

Le fichier `Tableaux_Methodes_Suivi_Stock_v1.ods` remis dans la conversation reste une maquette à cumuls manuels, comme indiqué dans l'audit du 9 novembre.

Le véritable fichier `Tableaux_Methodes_Suivi_Stock_v2_1.ods` décrit par le journal de tests n'a pas été retrouvé :
- il n'apparaît pas dans l'arborescence complète de la branche `main` (17 entrées examinées) ;
- une recherche par nom exact dans la bibliothèque et les fichiers de conversation n'a renvoyé aucun résultat.

Cela ne prouve pas qu'il n'existe nulle part ailleurs ; cela signifie qu'il n'est pas récupérable dans les emplacements contrôlés pendant cette vérification. Les journaux de tests restent des documents de preuve déclarative tant que le fichier binaire correspondant n'est pas retrouvé et rouvert.

## 4. Décision de production

1. Ne pas confondre le pack XLSX existant avec le stock automatisé v2.1.
2. Utiliser le pack multi-suivi comme référence fonctionnelle pour les listes et la structure, pas comme livrable LibreOffice validé.
3. Pour le produit Stock, conserver l'exigence d'un journal de mouvements qui recalcule réellement les quantités par référence.
4. Pour le produit Maintenance, réutiliser les règles d'échéance déjà présentes comme base de test, en gardant la mise à jour de la dernière intervention manuelle clairement documentée en version 1.
5. Avant diffusion, produire les versions ODS, recalculer et rouvrir les fichiers dans LibreOffice Calc, tester les validations, les filtres, les cellules vides et les seuils, puis faire un essai utilisateur.

## 5. État commercial

Ces deux XLSX sont des ressources de travail retrouvées dans la bibliothèque, pas des produits ODS finalisés. Aucun fichier n'a été envoyé à un client. Aucun contact commercial, dépense ou engagement juridique n'a été effectué dans le cadre de cet inventaire.
