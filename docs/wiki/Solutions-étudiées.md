# Solutions étudiées

## DocuSeal

DocuSeal a été retenu et installé pour expérimenter la préparation des documents et la signature électronique.

**Avantages observés pour le projet :**
- Déploiement possible avec Docker.
- Interface web.
- Gestion de modèles et d'invitations.
- Accès au parcours de signature depuis un navigateur mobile lors du test.

**Points à traiter :**
- Vérification des champs du modèle PDF.
- Intégration avec le backend.
- Sécurisation de l'accès public.
- Validation du parcours complet et des besoins de l'établissement.

## Docker

Docker permet d'exécuter DocuSeal dans un conteneur isolé et de conserver ses données dans un volume nommé. Cette solution a été utilisée pour le prototype.

## Brevo SMTP

Brevo a été utilisé comme relais SMTP pour l'envoi des invitations. La réception d'un e-mail de test a été confirmée.

## Technologies envisagées pour le développement

| Technologie | Utilisation envisagée |
|---|---|
| PHP | Backend et API |
| MySQL / MariaDB | Base de données métier |
| Kotlin ou Java | Application Android |
| Debian | Serveur |
| Docker | Déploiement des services |
| HTTPS | Protection des échanges |

## Hébergement

Le besoin d'hébergement étudié porte sur un serveur situé en France, avec au minimum 4 cœurs CPU et 8 Go de RAM. Des fournisseurs ont été comparés dans le cadre de l'étude : OVHcloud, LWS, Scaleway et OnetSolutions.

Le choix définitif doit être basé sur les offres réellement disponibles, le coût, les sauvegardes, le support, la localisation des données et les besoins de disponibilité. La comparaison ne signifie pas qu'un contrat ou un serveur chez chacun de ces fournisseurs a été souscrit.

## Conclusion

Le prototype s'appuie sur DocuSeal, Docker et Brevo pour valider le circuit documentaire et les invitations. PHP, MySQL/MariaDB et Android constituent l'architecture applicative cible à finaliser.
