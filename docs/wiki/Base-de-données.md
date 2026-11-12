# Base de données

## Rôle

La base de données doit conserver les informations nécessaires au suivi des conventions : élèves, entreprises, périodes de stage, utilisateurs, signataires et état des signatures.

Le choix technique envisagé est **MySQL ou MariaDB**. Une base de travail nommée `conventions_stage` a été évoquée pendant la préparation du backend PHP local.

> **État :** la structure définitive et la connexion intégrée à l'application ne sont pas confirmées comme terminées. Les éléments ci-dessous décrivent le modèle fonctionnel à mettre en place, pas un schéma SQL déjà validé.

## Entités envisagées

| Entité | Informations principales |
|---|---|
| Élève | Identité et classe |
| Entreprise | Nom, adresse et coordonnées utiles |
| Tuteur | Identité et coordonnées du tuteur |
| Convention | Élève, entreprise, dates, document et état |
| Utilisateur | Compte, rôle et droits |
| Signataire | Rôle, identité, adresse e-mail et ordre éventuel |
| Signature | État, date et référence de la procédure |
| Document | Nom, emplacement et lien avec la convention |

## Relations fonctionnelles

- Un élève peut avoir plusieurs conventions au fil de sa scolarité.
- Une convention est associée à un élève et à une entreprise.
- Une convention comporte plusieurs signataires.
- Chaque signataire est associé à une étape de signature.
- Une convention peut être liée à un ou plusieurs documents.

## Principes de sécurité

- Ne pas enregistrer les mots de passe en clair.
- Utiliser des requêtes préparées avec PDO côté PHP.
- Vérifier les droits avant de consulter ou modifier une convention.
- Éviter de stocker inutilement des données personnelles.
- Protéger les documents et les sauvegardes.
- Définir une politique de conservation et de suppression.

## À compléter

- Schéma relationnel définitif.
- Clés primaires et étrangères.
- Contraintes d'intégrité.
- Script de création SQL.
- Politique de sauvegarde et de restauration.
