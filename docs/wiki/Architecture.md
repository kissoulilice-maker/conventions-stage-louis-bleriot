# Architecture technique

## Vue d'ensemble

L'architecture cible est organisée autour d'un serveur central et de plusieurs composants.

```text
Application Android
        |
        | HTTPS / API REST (prévu)
        v
Backend PHP (prévu)
        |
        +------> Base MySQL / MariaDB (prévue)
        |
        +------> DocuSeal (installé et testé)
                       |
                       +----> Invitations par e-mail
                              via SMTP Brevo (testé)
```

## Composants

| Composant | Rôle | État |
|---|---|---|
| Serveur Debian | Héberger les services | Environnement de test utilisé |
| Docker | Exécuter DocuSeal | Utilisé |
| DocuSeal | Modèles et circuit de signature | Installé et testé |
| Brevo SMTP | Envoyer les invitations | Envoi testé |
| Backend PHP | API et logique métier | Prévu / intégration à réaliser |
| MySQL ou MariaDB | Stockage métier | Prévu / intégration à réaliser |
| Application Android | Interface mobile | Projet prévu, liaison backend à finaliser |
| HTTPS | Chiffrement des accès | À mettre en place avant production |

## Serveur et conteneur

DocuSeal a été lancé dans un conteneur Docker nommé `docuseal`, avec une publication du port hôte 3000 vers le port 3000 du conteneur et un volume nommé `docuseal-data` monté dans `/data`.

Commande de lancement utilisée pendant les essais :

```bash
docker run --name docuseal -p 3000:3000 -v docuseal-data:/data docuseal/docuseal
```

Sur le serveur, les commandes Docker ont été exécutées avec `sudo` lorsque le compte SSH ne disposait pas encore des droits du groupe Docker.

## Flux de données cible

1. L'application transmet les informations au backend PHP.
2. Le backend valide les données et les enregistre dans la base.
3. Le backend prépare ou transmet le document à DocuSeal.
4. DocuSeal gère les étapes de signature et les invitations.
5. Le backend récupère ou consulte l'état de la procédure.
6. L'application affiche l'avancement à l'utilisateur.

Ce flux décrit l'architecture cible ; son automatisation complète reste à réaliser et à vérifier.

## Sécurité

- Utiliser HTTPS pour les échanges externes.
- Ne jamais exposer directement la base de données à Internet.
- Protéger les comptes et secrets de configuration.
- Limiter les droits des comptes système et applicatifs.
- Sauvegarder les documents et les données.
- Contrôler les autorisations selon le rôle de chaque utilisateur.
