# Cahier des charges — Modèle de suivi de stock

**Produit :** Suivi de stock simple  
**Prix de lancement envisagé :** 20 €  
**Format cible :** LibreOffice Calc (.ods) ; compatibilité Excel à tester avant de la promettre  
**Statut au 8 novembre 2026 :** le prototype ODS v1 existe localement et a été recalculé avec LibreOffice. Sur les exemples fictifs, les calculs du stock actuel, les alertes et les indicateurs du tableau de bord ont été vérifiés. Les colonnes Entrées cumulées et Sorties cumulées sont toutefois saisies manuellement : le journal Mouvements ne les alimente pas. Le fichier n’est pas versionné dans le dépôt GitHub. Les filtres ne sont pas préconfigurés, les listes de l’onglet Listes ne sont pas encore des menus déroulants et la compatibilité Excel n’a pas été testée. Une tentative de version automatisant les mouvements n’a pas passé le contrôle de recalcul dans le classeur complet ; elle n’est donc pas retenue comme livrable.

## Objectif

Permettre à un artisan, une petite entreprise technique ou une association de connaître rapidement les quantités disponibles et de repérer les articles à recommander, sans logiciel métier ni abonnement.

## Structure du classeur

### Feuille 1 — « Stock »

Une ligne par référence, avec ces colonnes :

| Colonne | Nom | Utilisation |
|---|---|---|
| A | Référence | Identifiant interne unique |
| B | Article | Nom compréhensible |
| C | Catégorie | Famille d'articles |
| D | Emplacement | Atelier, véhicule, réserve, etc. |
| E | Fournisseur | Nom du fournisseur habituel |
| F | Quantité initiale | Quantité au démarrage |
| G | Entrées | Quantités reçues depuis le démarrage |
| H | Sorties | Quantités consommées ou sorties |
| I | Stock actuel | Calcul automatique |
| J | Seuil d'alerte | Niveau minimal défini par l'utilisateur |
| K | À commander ? | Alerte automatique |
| L | Dernière mise à jour | Date de contrôle manuel |
| M | Commentaires | Informations facultatives |

### Formules prévues

À partir de la ligne 2, avec des cellules vides traitées comme zéro :

- **Stock actuel (I2)** : `=F2+G2-H2`
- **Alerte (K2)** : `=IF(I2<=J2;"À COMMANDER";"OK")`

La formule d'alerte devra être localisée selon la langue de l'application (par exemple `SI` en interface française) et testée dans LibreOffice Calc. Les formules ci-dessus sont une logique de référence, pas encore validée dans un fichier.

### Feuille 2 — « Mouvements »

Pour tracer chaque opération :

| Colonne | Nom | Utilisation |
|---|---|---|
| A | Date | Date du mouvement |
| B | Référence | Référence de l'article |
| C | Article | Libellé |
| D | Type | Entrée ou sortie |
| E | Quantité | Quantité déplacée |
| F | Motif | Achat, utilisation, retour, correction |
| G | Personne / service | Facultatif |
| H | Commentaire | Facultatif |

**Limite importante :** la première version peut utiliser des totaux saisis manuellement dans « Stock ». Pour automatiser le calcul depuis « Mouvements », il faudra ajouter des formules de synthèse par référence et tester les cas d'erreur (référence inconnue, quantité négative, cellules vides). Ne pas vendre une fonctionnalité tant qu'elle n'est pas testée.

### Feuille 3 — « Guide »

- Commencer par remplacer les exemples fictifs par les articles de l'utilisateur.
- Donner une référence différente à chaque article.
- Saisir la quantité initiale et le seuil d'alerte.
- Mettre à jour les entrées et sorties, puis vérifier le stock physique.
- Contrôler régulièrement la colonne « Dernière mise à jour ».
- Faire une copie de sauvegarde avant toute modification importante.
- Ne pas utiliser ce modèle comme système comptable ou de traçabilité réglementaire sans adaptation professionnelle.

## Qualité et présentation

- Première ligne figée et filtres activés.
- Titres explicites, largeur de colonnes adaptée, format de date homogène.
- Mise en évidence visuelle des stocks à commander.
- Validation de données pour les catégories et les types de mouvement, si possible.
- 5 à 10 lignes d'exemple fictives clairement signalées.
- Aucun nom, e-mail ou donnée d'une vraie entreprise dans le fichier de démonstration.
- Une page d'instructions claire, sans macros obligatoires.

## Tests avant vente

1. Vérifier que les quantités calculées ne deviennent pas négatives sans signalement.
2. Tester une référence sans mouvement, une entrée, une sortie et un stock sous le seuil.
3. Tester les filtres et la copie des formules sur plusieurs lignes.
4. Ouvrir, enregistrer et rouvrir le fichier dans LibreOffice Calc.
5. Si une version Excel est annoncée, ouvrir et tester séparément dans Excel.
6. Tester les cellules vides et les erreurs de saisie.
7. Vérifier que le guide suffit à une personne non technique.

## À faire ensuite

1. Conserver le prototype v1 comme démonstration locale, sans le présenter comme un stock automatiquement synchronisé.
2. Isoler puis corriger le défaut de recalcul des formules inter-feuilles dans une nouvelle version ; ne remplacer v1 qu'après réussite des tests dans le classeur complet.
3. Préconfigurer et tester les filtres et validations de saisie dans LibreOffice Calc.
4. Ajouter une capture d'écran ou un aperçu au site, sans prétendre qu'il s'agit d'un fichier téléchargeable tant que le fichier n'est pas publié par un canal public vérifié.
5. Fixer clairement les limites incluses dans le prix de 20 € et facturer séparément toute personnalisation supplémentaire.
