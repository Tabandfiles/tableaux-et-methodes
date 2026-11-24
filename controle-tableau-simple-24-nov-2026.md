# Contrôle partiel du Tableau simple — 24 novembre 2026

## Périmètre

Contrôle réalisé sur des copies temporaires des deux fichiers du pack local du 23/11/2026, avec LibreOffice Calc 25.2.3.2 en mode headless via UNO. Les fichiers de référence n'ont pas été modifiés.

## Résultats vérifiés

| Contrôle | Démonstration | Version vierge |
|---|---|---|
| Ouverture ODS | Réussie | Réussie |
| Feuilles Guide / Suivi / Listes | Présentes | Présentes |
| Capacité prévue | 50 lignes de saisie | 50 lignes de saisie |
| Données de démonstration | 6 demandes | 0 demande |
| Validation Priorité en F5 et F54 | Liste `Priorites` présente | Liste `Priorites` présente |
| Validation Statut en H5 et H54 | Liste `Statuts` présente | Liste `Statuts` présente |
| Messages d'erreur | Configurés | Configurés |
| Copie temporaire d'une cellule de priorité | Validation conservée | Validation conservée |
| Enregistrement ODS puis réouverture | Réussi | Réussi |
| Validation après réouverture | Conservée sur première et dernière ligne | Conservée sur première et dernière ligne |
| Export PDF depuis Calc | 2 pages A4 | 3 pages A4 |

Le XML ODS déclare une plage de filtre `Suivi.A4:I54` avec boutons de filtre. Les menus de filtre n'ont pas été manipulés au clic.

Les PDF exportés ont été rendus en images et inspectés : le guide tient sur une page ; la feuille Suivi est lisible. La version vierge répartit les 50 lignes sur deux pages de tableau, sans données de démonstration.

## Tests non réalisés

- Sélection réelle dans les listes déroulantes avec la souris.
- Saisie d'une valeur interdite et observation du blocage effectif.
- Manipulation réelle des filtres et du tri dans l'interface.
- Copier-coller manuel par un utilisateur.
- Test par une personne extérieure.
- Compatibilité Excel.
- Impression sur imprimante physique.

## Conclusion

Les contrôles structurels, la persistance des validations après sauvegarde/réouverture et l'export PDF sont vérifiés. **Le Tableau simple n'est pas déclaré prêt à la vente** : les interactions dans l'interface graphique et le test utilisateur restent nécessaires.
