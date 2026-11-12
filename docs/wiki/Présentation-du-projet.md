# Présentation du projet DocuBlériot

## Contexte

La gestion des conventions de stage implique plusieurs personnes : l'établissement, l'équipe pédagogique, l'entreprise d'accueil et la famille ou l'étudiant majeur. Les documents doivent être transmis, vérifiés, signés puis conservés.

DocuBlériot vise à centraliser ce parcours et à limiter les impressions, les déplacements et les échanges de documents par différents canaux.

## Principe

Le projet s'appuie sur plusieurs briques complémentaires :

- **DocuSeal** : outil de préparation et de signature électronique des documents.
- **Serveur Debian** : environnement serveur de test et d'hébergement du service DocuSeal.
- **Docker** : exécution du conteneur DocuSeal.
- **Brevo SMTP** : service utilisé pour tester l'envoi des invitations par e-mail.
- **PHP et MySQL/MariaDB** : technologies envisagées pour le futur backend et le stockage des données.
- **Android (Kotlin ou Java)** : application mobile envisagée pour consulter les conventions et communiquer avec le backend.

## État d'avancement

### Réalisé ou testé

- Installation et démarrage de DocuSeal avec Docker.
- Exposition de DocuSeal sur le port 3000 pour les essais.
- Utilisation d'un volume Docker nommé `docuseal-data` pour conserver les données.
- Création de modèles de démonstration et d'un modèle nommé « Convention PFMP – DocuBlériot ».
- Configuration d'un relais SMTP Brevo en STARTTLS sur le port 587.
- Test de réception d'une invitation de signature.
- Test d'ouverture du parcours de signature depuis un navigateur mobile.
- Connexion au serveur Debian par SSH et vérifications Docker avec les droits administrateur.

### Prévu ou à finaliser

- Développement et sécurisation de l'API PHP.
- Création et intégration de la base MySQL/MariaDB.
- Connexion complète de l'application Android à l'API.
- Liaison automatisée entre les données de convention et DocuSeal.
- Mise en place d'un accès HTTPS en production.
- Validation complète du parcours à cinq signataires et de l'archivage.

## Périmètre

Le prototype technique ne doit pas être confondu avec un service de production : les tests réalisés valident certaines briques, mais ne prouvent pas encore que l'ensemble du processus est automatisé et opérationnel pour toutes les classes.
