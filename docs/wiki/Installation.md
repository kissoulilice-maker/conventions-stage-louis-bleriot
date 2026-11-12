# Installation et environnement de test

## Environnement utilisé

- Système serveur : Debian (environnement mentionné : Debian Trixie).
- Conteneurisation : Docker.
- Service : image `docuseal/docuseal`.
- Nom du conteneur : `docuseal`.
- Port publié : `3000:3000`.
- Volume persistant : `docuseal-data`.

## Lancement de DocuSeal

La commande utilisée pendant les essais :

```bash
docker run --name docuseal -p 3000:3000 -v docuseal-data:/data docuseal/docuseal
```

Le volume nommé permet de conserver les données de DocuSeal indépendamment du cycle de vie du conteneur.

## Vérifier le conteneur

```bash
sudo docker ps
sudo docker logs docuseal
```

La commande `sudo` a été nécessaire sur le compte SSH utilisé, car celui-ci ne disposait pas initialement des permissions Docker.

L'ajout d'un utilisateur au groupe `docker` est possible, mais ce groupe donne des privilèges très élevés, proches de ceux de l'administrateur. Cette décision doit être prise en connaissance de cause.

## Connexion au serveur

L'accès d'administration au serveur a été effectué par SSH depuis Git Bash sous Windows.

Exemple de syntaxe (adapter le compte et l'adresse du serveur) :

```bash
ssh UTILISATEUR@ADRESSE_DU_SERVEUR
```

Ne pas publier l'adresse IP, les clés privées ou les identifiants dans la documentation publique.

## SMTP Brevo

La configuration d'essai utilise le relais `smtp-relay.brevo.com`, le port `587` et STARTTLS avec authentification. Les identifiants doivent rester dans une configuration protégée et ne doivent pas être ajoutés au dépôt Git.

## Points indispensables avant production

- Mettre en place un nom de domaine et HTTPS.
- Ne pas exposer le port de test sans protection adaptée.
- Limiter les ports ouverts au strict nécessaire.
- Mettre à jour régulièrement Debian, Docker et DocuSeal.
- Prévoir sauvegardes et restauration.
- Protéger les secrets et les comptes d'administration.
- Tester les droits d'accès et la confidentialité des conventions.

**Important :** l'accès HTTP sur le port 3000 correspond aux essais. Il ne constitue pas une configuration de production sécurisée.
