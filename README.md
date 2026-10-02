# Gestion dématérialisée des conventions de stage

## Lycée Louis Blériot

### Dépôt GitHub du projet

Le code source et la documentation du projet sont disponibles sur
le dépôt GitHub :

**GitHub :** [conventions-stage-louis-bleriot](https://github.com/TON-PSEUDO/conventions-stage-louis-bleriot)

## Présentation du projet

Ce projet a pour objectif de mettre en place une solution permettant
de gérer les conventions de stage de manière dématérialisée.

L'application doit permettre de créer, gérer, suivre, valider et
faire signer les conventions de stage.

---

### Objectifs détaillés du projet

- Dématérialiser les conventions de stage.
- Faciliter la création des conventions.
- Permettre le suivi de l'état des conventions.
- Mettre en place un système de validation.
- Gérer les différentes signatures.
- Centraliser les documents.
- Faciliter le travail des élèves, des entreprises et du personnel
  du lycée.
- Améliorer le suivi des conventions.

---

## Solutions et logiciels étudiés

### 1. ESUP-Stage

**GitHub :**  
[https://github.com/EsupPortail/esup-stage](https://github.com/EsupPortail/esup-stage)

ESUP-Stage est une solution open source destinée à la gestion des
stages et des conventions.

Cette solution constitue la première solution étudiée pour le projet.

L'étude porte notamment sur :

- la gestion des stages ;
- la création des conventions ;
- le processus de validation ;
- l'architecture de l'application ;
- les possibilités d'adaptation aux besoins du lycée.

---

### 2. Documenso

**Documentation :**  
[https://docs.documenso.com/](https://docs.documenso.com/)

**GitHub :**  
[https://github.com/documenso/documenso](https://github.com/documenso/documenso)

Documenso est une solution open source de signature électronique.

Elle est étudiée afin de gérer la partie signature des conventions.

La convention comporte 5 emplacements de signature :

1. Chef d'établissement
2. Représentant de l'entreprise
3. Élève ou représentant légal
4. Enseignant référent
5. Tuteur en entreprise

---

### 3. Application personnalisée

Une application personnalisée est développée pour répondre aux
besoins spécifiques du lycée Louis Blériot.

Technologies utilisées ou envisagées :

- PHP
- MySQL / MariaDB
- HTML
- CSS
- JavaScript
- XAMPP

L'application permet progressivement de mettre en place :

- un espace élève ;
- un espace entreprise ;
- un espace personnel du lycée ;
- la gestion des conventions ;
- le suivi des signatures ;
- la gestion des utilisateurs ;
- l'historique des actions.

---

## Outils de conception

### Excalidraw

**GitHub :**  
[https://github.com/excalidraw/excalidraw](https://github.com/excalidraw/excalidraw)

Excalidraw est un outil open source permettant de créer des schémas
et de représenter visuellement l'architecture et le fonctionnement
du projet.

Il peut notamment servir à réaliser :

- des schémas d'architecture ;
- des maquettes ;
- des diagrammes fonctionnels ;
- des représentations du fonctionnement de l'application.

---

### Mermaid

**GitHub :**  
[https://github.com/mermaid-js/mermaid](https://github.com/mermaid-js/mermaid)

Mermaid est une bibliothèque open source permettant de créer des
diagrammes directement à partir de texte.

Il peut être utilisé pour représenter :

- des diagrammes de séquence ;
- des organigrammes ;
- des diagrammes de flux ;
- des architectures ;
- des diagrammes de classes.

---

### yEd

**Site officiel :**  
[https://www.yworks.com/products/yed](https://www.yworks.com/products/yed)

yEd est un logiciel permettant de créer différents types de
diagrammes.

Il peut être utilisé pour réaliser :

- des diagrammes UML ;
- des organigrammes ;
- des schémas réseau ;
- des diagrammes d'architecture.

yEd n'est pas open source et ne possède donc pas de dépôt GitHub
officiel.

---

### draw.io / diagrams.net

**GitHub :**  
[https://github.com/jgraph/drawio](https://github.com/jgraph/drawio)

draw.io, également appelé diagrams.net, est un outil permettant
de créer différents types de diagrammes.

Il peut notamment être utilisé pour :

- les diagrammes UML ;
- les schémas réseau ;
- les diagrammes de flux ;
- les architectures techniques ;
- les modèles de bases de données.

---

## Architecture envisagée

```text
                    Utilisateurs
                         │
        ┌────────────────┼────────────────┐
        │                │                │
      Élève          Personnel        Entreprise
        │                │                │
        └────────────────┼────────────────┘
                         │
                         ▼
              Application Web PHP
                         │
                         ▼
                   Base MySQL
                         │
                         ▼
                  Convention PDF
                         │
                         ▼
                     Documenso
                         │
                         ▼
                  5 signatures
                         │
                         ▼
              Convention finalisée
