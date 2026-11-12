# DocuSeal

## Présentation

DocuSeal est le service retenu pour préparer des documents et gérer leur circuit de signature électronique dans DocuBlériot.

## Installation réalisée

DocuSeal a été lancé sur le serveur avec Docker dans un conteneur nommé `docuseal`.

- Port utilisé pendant les essais : `3000`.
- Volume Docker : `docuseal-data`.
- Répertoire de données du conteneur : `/data`.

Commande utilisée :

```bash
docker run --name docuseal -p 3000:3000 -v docuseal-data:/data docuseal/docuseal
```

Le démarrage a affiché les migrations de base de données puis le lancement du serveur web DocuSeal.

## Modèles créés

Deux modèles ont été utilisés pendant les essais :

- **Convention de démonstration** : modèle de test utilisé notamment pour vérifier l'envoi d'une invitation.
- **Convention PFMP – DocuBlériot** : modèle destiné au projet, associé à cinq rôles de signataires.

Un contrôle de l'API a toutefois renvoyé une liste de champs vide (`fields: []`) pour le modèle PFMP à ce moment-là. Le positionnement et la validation de tous les champs de signature doivent donc être revérifiés dans l'interface DocuSeal avant de considérer le modèle comme finalisé.

## Signataires prévus

1. Professeur référent.
2. Tuteur de stage.
3. Directeur.
4. Entreprise.
5. Responsable légal ou étudiant majeur.

Les rôles exacts et leur ordre doivent être confirmés avec le fonctionnement administratif retenu par l'établissement.

## E-mails

Le relais SMTP Brevo a été configuré pour les essais :

| Paramètre | Valeur |
|---|---|
| Serveur SMTP | `smtp-relay.brevo.com` |
| Port | `587` |
| Sécurité | STARTTLS |
| Authentification | LOGIN |

Un e-mail d'invitation a été reçu lors d'un test. Les secrets SMTP ne doivent jamais être publiés dans le Wiki ou dans le dépôt.

## Accès mobile

L'ouverture d'une invitation DocuSeal depuis un navigateur mobile a été testée. Cela valide l'accès au parcours de signature depuis un téléphone pour ce scénario de démonstration, mais ne valide pas encore l'intégration native avec l'application Android.

## Points à finaliser

- Vérifier les champs et leur position sur le PDF.
- Tester le parcours complet avec les cinq signataires.
- Vérifier le PDF final et les preuves associées.
- Relier le backend PHP à DocuSeal.
- Configurer HTTPS et les paramètres de production.
