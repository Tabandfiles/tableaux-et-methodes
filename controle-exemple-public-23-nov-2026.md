# Contrôle et publication de l’aperçu Tableau simple — 23 novembre 2026

Site contrôlé : https://tabandfiles.github.io/tableaux-et-methodes/

## État initial vérifié
- Dépôt public : `Tabandfiles/tableaux-et-methodes`, branche `main`.
- Dernier commit avant intervention : `23753cead6e27951a18915c8d8c9b0f233144948`.
- Dernier déploiement Pages avant intervention : run 180, terminé avec succès le 22/11/2026.
- Le site présentait déjà cinq aperçus, mais l’exemple de maintenance n’affichait pas les identifiants d’équipement du classeur.
- Le pack ODS du Tableau simple était local et non téléchargeable ; aucun fichier ODS n’est publié par cette mise à jour.

## Travail effectué
1. Création d’un aperçu PDF A4 paysage d’une page, à partir des six lignes fictives de l’onglet `Suivi` du classeur Tableau simple.
2. Le PDF reprend les libellés exacts du classeur : priorités Basse / Normale / Haute / Urgente et statuts À traiter / En cours / En attente / Terminé / Annulé.
3. Le PDF présente les capacités prévues (50 lignes), les filtres, les listes déroulantes et les limites (pas de rappel, d’e-mail, de multi-utilisateur ni de connexion externe).
4. Publication du PDF dans `exemples/suivi-demandes-apercu.pdf`.
5. Mise à jour de la page : l’offre Tableau simple est distinguée des trois modèles automatisés encore en préparation ; un lien vers l’aperçu PDF est ajouté.
6. Correction des identifiants de l’exemple Maintenance pour correspondre au classeur : POM-001, CTA-002 et VAN-003.
7. Suppression d’une séquence littérale `\\n` présente entre deux cartes d’aperçu HTML.
8. Actualisation du sitemap et du README.

## Contrôles effectués
- Le PDF local fait 4 533 octets, une page A4 paysage.
- Le PDF a été converti en image et inspecté visuellement : tableau complet, textes lisibles, aucune coupure de cellule ni débordement détecté.
- Le texte extrait du PDF confirme les six références DEM-001 à DEM-006 et les statuts exacts du classeur.
- Les données de démonstration sont fictives.
- Le workflow GitHub Pages n°181 (run 45243506032) a terminé avec succès le 23/11/2026 à 18:56 UTC : https://github.com/Tabandfiles/tableaux-et-methodes/actions/runs/45243506032.
- Après déploiement, la page publique a été relue : le lien PDF est présent dans la carte Tableau simple, les identifiants POM-001 / CTA-002 / VAN-003 sont affichés et la séquence littérale `\\n` a disparu.
- Une session navigateur en direct a retrouvé le lien PDF et confirmé son URL publique. L’ouverture / lecture directe du PDF par le navigateur automatisé n’est pas prise en charge ; le fichier local a toutefois été contrôlé par extraction de texte et inspection visuelle.

## Limites
- L’aperçu PDF ne remplace pas le classeur ODS.
- Le pack ODS reste local ; aucun téléchargement ODS public n’est proposé.
- Le test visuel au clic dans Calc, Excel et un test utilisateur extérieur restent à faire.
- Les trois modèles automatisés (stock, interventions, maintenance) restent non disponibles à la livraison.
- Aucun prospect n’a été ajouté lors de ce contrôle ; la base nationale existante reste à requalifier individuellement avant tout contact.
- Aucun e-mail, appel ou formulaire commercial envoyé ; aucune dépense ni engagement juridique.
