# Évolutions prévues

Cette page distingue les prochaines étapes des fonctions déjà testées.

## Priorité 1 — Fiabiliser DocuSeal

- Vérifier les champs de signature du modèle « Convention PFMP – DocuBlériot ».
- Réaliser un essai complet avec les cinq rôles.
- Vérifier le document final généré.
- Vérifier les relances et le suivi des invitations.

## Priorité 2 — Sécuriser le serveur

- Associer un nom de domaine au service.
- Configurer HTTPS avec un certificat valide.
- Réduire l'exposition réseau aux seuls ports nécessaires.
- Organiser les mises à jour.
- Mettre en place des sauvegardes et tester leur restauration.
- Protéger les identifiants SMTP et les secrets applicatifs.

## Priorité 3 — Développer le backend

- Développer l'API PHP.
- Définir les routes nécessaires à la gestion des conventions.
- Mettre en place la validation des données.
- Connecter MySQL/MariaDB.
- Relier les opérations du backend à DocuSeal.
- Gérer les erreurs et les états de signature.

## Priorité 4 — Développer l'application Android

- Créer les écrans de connexion et d'accueil.
- Afficher la liste des conventions.
- Afficher le détail d'une convention et son état.
- Permettre la consultation des documents.
- Connecter l'application à l'API sécurisée.
- Gérer les erreurs réseau et les sessions.

Un prototype Android V3 a été envisagé avec des écrans d'accueil, documents, détail, formulaire, signature et profil. Une première approche avec données locales et documents de démonstration a été décrite ; la liaison réelle Android → PHP → MySQL reste à finaliser. DocuSeal n'était pas encore connecté dans cette proposition de prototype.

## Priorité 5 — Tests et mise en service

- Tester les rôles et les autorisations.
- Tester le parcours complet avec plusieurs conventions.
- Vérifier l'expérience sur téléphone et ordinateur.
- Tester les cas d'erreur : adresse e-mail incorrecte, invitation non reçue, signature en attente, document incomplet.
- Définir l'archivage, la durée de conservation et les procédures de support.
- Faire valider le processus par l'établissement avant un usage réel.

## Critère de fin

Le projet sera prêt pour une mise en service lorsque le parcours complet sera intégré, sécurisé, documenté et validé par des essais représentatifs.
