# Guide de recette externe — Tableau simple

**Version concernée :** prototype Tableau simple v1.1  
**Application cible :** LibreOffice Calc  
**Statut :** protocole préparé le 26/11/2026 ; aucun essai externe n'est déclaré réalisé.

## Consignes au testeur

1. Travailler uniquement sur des copies des fichiers de démonstration et vierge ; conserver les originaux intacts.
2. Utiliser uniquement les données fictives fournies. Ne pas saisir de données personnelles ou confidentielles.
3. Noter la version de LibreOffice Calc et le système utilisé.
4. Pour chaque essai, inscrire **Réussi**, **Échoué** ou **Non testé**, puis décrire précisément le résultat observé.
5. Ne pas supposer qu'une valeur non autorisée est bloquée : noter si Calc refuse la saisie, affiche un avertissement ou l'accepte.

## Scénario de test

| ID | Manipulation | Résultat attendu / point à observer | Résultat |
|---|---|---|---|
| TS-01 | Ouvrir une copie du fichier de démonstration, l'enregistrer sous un autre nom, fermer puis rouvrir | Le fichier s'ouvre sans réparation ; les feuilles, formats et données sont conservés | À renseigner |
| TS-02 | Cliquer dans une cellule Priorité d'une ligne de saisie | Une liste propose les priorités documentées dans le guide | À renseigner |
| TS-03 | Cliquer dans une cellule Statut | Une liste propose les statuts documentés dans le guide | À renseigner |
| TS-04 | Essayer de saisir une valeur absente de la liste dans Priorité puis Statut | Noter le comportement réel : refus, avertissement ou acceptation ; ne pas conclure sans essai | À renseigner |
| TS-05 | Filtrer le tableau sur le statut « En cours » | Les lignes visibles correspondent au statut choisi ; les cellules d'une ligne restent associées | À renseigner |
| TS-06 | Trier les demandes par date cible | Les données de chaque demande restent sur la même ligne après tri | À renseigner |
| TS-07 | Copier une ligne de demande dans une autre ligne libre | Les données, formats et validations restent cohérents ; vérifier les listes déroulantes dans la ligne copiée | À renseigner |
| TS-08 | Saisir une demande fictive sur la dernière ligne prévue (50e ligne de saisie, ligne 54 de la feuille) | La mise en forme et les validations sont encore présentes | À renseigner |
| TS-09 | Ouvrir une copie du fichier vierge | Aucune demande fictive ne subsiste ; guide et listes sont présents | À renseigner |
| TS-10 | Exporter la démonstration et le fichier vierge en PDF | Pas de page blanche ; titres et colonnes utiles lisibles ; les 50 lignes prévues sont imprimées dans le fichier vierge | À renseigner |

## Informations à relever

- Système d'exploitation :
- Version exacte de LibreOffice Calc :
- Fichier testé (démonstration ou vierge) :
- Date du test :
- Résultat général :
- Problèmes observés (étapes et reproduction) :
- Améliorations suggérées :

## Critères de validation

Le Tableau simple ne pourra être déclaré prêt à la livraison qu'après réussite des tests critiques, correction ou documentation des défauts, inspection du rendu écran et PDF, et essai par une personne extérieure au projet. La compatibilité Microsoft Excel reste non annoncée tant qu'un test dédié n'a pas été réalisé.

**Ce guide prépare une recette indépendante ; il ne constitue pas une preuve qu'un testeur a utilisé le classeur.**
