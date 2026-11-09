# Grille de contrôle qualité — tableurs Tableaux & Méthodes

**Version :** 1.1 — 8 novembre 2026  
**Usage :** contrôle interne avant de proposer ou livrer un fichier.  
**Statut :** checklist préparée ; elle ne signifie pas que les modèles sont déjà construits ou testés.

## 1. Définition du besoin

- [ ] Utilisateur et contexte identifiés.
- [ ] Logiciel cible confirmé (LibreOffice Calc en priorité ; Excel uniquement après test séparé).
- [ ] Colonnes et définitions comprises par une personne non technique.
- [ ] Périmètre, exclusions, format et prix annoncés avant réalisation.
- [ ] Pas de macro, script ou connexion externe inutile.
- [ ] Données de démonstration fictives uniquement.

## 2. Calculs et formules

- [ ] Chaque formule est testée avec un cas normal.
- [ ] Les cellules vides sont traitées comme prévu.
- [ ] Les limites (zéro, valeur négative, seuil exact, date manquante) sont testées.
- [ ] Les erreurs de saisie sont repérées ou documentées.
- [ ] Les formules restent correctes après copie sur plusieurs lignes.
- [ ] Les formules ne comptent pas les lignes entièrement vides.
- [ ] Les fonctions et séparateurs sont compatibles avec la langue et la version de Calc utilisée.
- [ ] Aucun calcul n'est annoncé comme automatique tant qu'il n'a pas été testé.

## 3. Ergonomie et fiabilité

- [ ] En-têtes explicites, ligne de titre figée et filtres activés.
- [ ] Formats cohérents : dates JJ/MM/AAAA, nombres et montants.
- [ ] Largeurs de colonnes adaptées, texte long lisible.
- [ ] Listes déroulantes testées si présentes.
- [ ] Tri et filtres ne désalignent jamais les lignes.
- [ ] Couleurs d'alerte accompagnées d'un libellé textuel.
- [ ] Impression ou export PDF lisible si c'est utile au client.
- [ ] Le fichier s'enregistre, se ferme et se rouvre sans avertissement inattendu.

## 4. Tests minimaux par produit

### Suivi de stock
- [ ] Article sans mouvement.
- [ ] Entrée seule.
- [ ] Sortie seule.
- [ ] Entrée puis sortie.
- [ ] Stock exactement égal au seuil.
- [ ] Stock inférieur au seuil.
- [ ] Quantité négative ou référence manquante signalée.
- [ ] Les mouvements et le stock affiché concordent avec le calcul manuel.

### Registre des interventions
- [ ] Intervention à planifier, en cours, en attente, terminée et annulée.
- [ ] Intervention urgente non terminée.
- [ ] Dates vides et dates inversées.
- [ ] Durée vide, nulle et négative.
- [ ] Les indicateurs excluent les lignes vides.
- [ ] Les filtres par statut, priorité, technicien et période fonctionnent.

### Suivi de maintenance
- [ ] Équipement sans échéance.
- [ ] Échéance passée, aujourd'hui et future.
- [ ] Intervention préventive terminée puis nouvelle échéance.
- [ ] Équipement retiré du service.
- [ ] Alerte de date testée avec une date de référence connue.
- [ ] Le modèle ne se présente pas comme une GMAO ou un outil de conformité réglementaire.

## 5. Compatibilité et livraison

- [ ] Ouvrir, modifier, enregistrer, fermer et rouvrir dans LibreOffice Calc.
- [ ] Si Excel est promis : ouvrir et tester séparément dans Excel.
- [ ] Vérifier les formules après téléchargement du fichier livré.
- [ ] Ajouter une notice courte avec les champs à modifier et les limites connues.
- [ ] Supprimer toute donnée personnelle ou commerciale utilisée pendant les tests.
- [ ] Préparer une copie vierge et une copie d'exemple fictif si utile.
- [ ] Vérifier le nom du fichier et la version avant envoi.

## 6. Règle de mise en vente

Ne pas présenter un produit comme prêt à vendre tant que les contrôles applicables ne sont pas cochés. Si un test échoue, documenter le défaut, corriger puis recommencer le test. Ne jamais annoncer une compatibilité, une automatisation ou une conformité non vérifiée.


## 7. Journal de contrôle — suivi de stock v1 (8 novembre 2026)

Le prototype local v1 a été ouvert et recalculé avec LibreOffice sur des données fictives.

| Cas contrôlé | Résultat observé | État |
|---|---|---|
| Sortie seule : stock initial 10, sortie 2 | Stock actuel 8 ; alerte « À COMMANDER » avec seuil 10 | Réussi |
| Entrée puis sortie : stock initial 20, entrée 10, sortie 6 | Stock actuel 24 ; alerte « OK » avec seuil 8 | Réussi |
| Sortie seule : stock initial 5, sortie 2 | Stock actuel 3 ; alerte « À COMMANDER » avec seuil 5 | Réussi |
| Indicateurs du tableau de bord sur les 3 exemples | 3 références, 2 alertes, 4 mouvements, quantité totale 35 | Réussi |

**Limites constatées :** les entrées et sorties cumulées sont saisies manuellement dans la feuille Stock ; le journal Mouvements ne les calcule pas automatiquement. Les tests de quantité négative, référence inconnue, seuil exactement atteint, cellules vides et extension de plage restent à faire. Les filtres et menus déroulants ne sont pas préconfigurés. La compatibilité Excel n'a pas été testée.

Une tentative d'automatisation inter-feuilles a produit des totaux nuls lors du recalcul du classeur complet. Cette version n'est pas acceptée et ne doit pas être livrée. Le produit reste un prototype, pas encore un modèle commercial final.


## 8. Journal de contrôle — suivi de stock v2.1 (9 novembre 2026)

Le modèle ODS v2.1 a été recalculé avec LibreOffice Calc sur des données fictives. Les tests statiques et les tests dynamiques sont consignés dans [tests-suivi-stock-v2-1.md](tests-suivi-stock-v2-1.md).

| Cas contrôlé | Résultat observé | État |
|---|---|---|
| Sortie seule | Stock 8 ; alerte À COMMANDER | Réussi |
| Entrée puis sortie | Stock 24 ; alerte OK | Réussi |
| Stock sous le seuil | Stock 3 ; alerte À COMMANDER | Réussi |
| Modification d'un mouvement | Le stock et l'alerte se recalculent | Réussi |
| Stock exactement égal au seuil | Alerte À COMMANDER | Réussi |
| Stock négatif | Alerte STOCK NÉGATIF | Réussi |
| Indicateurs et lignes vides | 3 références, 4 mouvements, 35 unités ; les lignes inutilisées ne sont pas comptées | Réussi |

**Limites non validées :** fonctionnement visuel des filtres dans une session Calc, menus déroulants, blocage des quantités négatives, détection des références inconnues ou dupliquées, compatibilité Excel et test utilisateur non technique. Ne pas cocher ces contrôles avant leur réalisation.
