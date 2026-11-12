# Fonctionnement

## Parcours fonctionnel cible

### 1. Préparation de la convention

Le document de convention est préparé à partir des informations de l'élève, de l'entreprise et de la période de stage. Il est ensuite importé ou préparé au format PDF.

### 2. Vérification du document

Les informations sont contrôlées et les emplacements nécessaires à la signature sont vérifiés dans DocuSeal.

### 3. Définition des signataires

La convention suit le circuit prévu par l'établissement, avec les cinq rôles suivants :

1. Professeur référent.
2. Tuteur de stage.
3. Directeur.
4. Entreprise.
5. Responsable légal ou étudiant majeur.

L'ordre exact du circuit doit être validé par l'établissement.

### 4. Envoi des invitations

DocuSeal envoie une invitation à chaque signataire par e-mail. Le relais SMTP Brevo a été configuré et un envoi d'essai a été reçu.

### 5. Signature

Le destinataire ouvre le lien d'invitation, consulte le document et suit les étapes proposées par DocuSeal. L'ouverture depuis un navigateur mobile a été testée.

### 6. Suivi

L'objectif est de consulter l'état de chaque étape et d'identifier les signatures encore attendues.

### 7. Finalisation

Lorsque le circuit est terminé, le document final doit pouvoir être récupéré puis archivé selon les règles de l'établissement.

## État des tests

| Élément | État constaté |
|---|---|
| Démarrage de DocuSeal sous Docker | Testé |
| Modèle de démonstration | Créé |
| Modèle « Convention PFMP – DocuBlériot » | Créé, champs à revérifier |
| Configuration SMTP Brevo | Testée |
| Réception d'une invitation | Testée |
| Ouverture depuis un téléphone | Testée |
| Circuit complet à cinq signatures | À valider |
| Automatisation PHP / base de données | À réaliser |
| Intégration Android complète | À réaliser |
| Archivage automatisé | À réaliser / valider |
