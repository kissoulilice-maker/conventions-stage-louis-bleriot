# Projet 2 — Gestion dématérialisée des conventions de stage

## Lycée Louis Blériot

Application destinée à dématérialiser la gestion des conventions de stage :
création, suivi, validation et signature des conventions.

---

## Solutions étudiées

### Solution 1 — ESUP-Stage

[ESUP-Stage](https://github.com/EsupPortail/esup-stage)

ESUP-Stage est une solution open source destinée à la gestion des stages.
Elle constitue la première solution étudiée dans le cadre du Projet 2.

Objectifs de l'étude :

- étudier les fonctionnalités proposées ;
- comprendre son architecture ;
- étudier son installation ;
- vérifier la gestion des conventions ;
- étudier le processus de validation ;
- étudier les possibilités de signature ;
- déterminer si la solution peut être adaptée aux besoins du lycée Louis Blériot.

---

### Solution 2 — Documenso

Documenso sera étudié comme solution open source
de signature électronique et pourra éventuellement être intégré
à notre application.

---

### Solution 3 — Développement personnalisé

Une application développée en PHP avec MySQL/MariaDB,
HTML, CSS et JavaScript.

Cette solution permettra d'adapter précisément l'application
aux besoins du lycée.

---

## Technologies envisagées

- PHP
- MySQL / MariaDB
- HTML
- CSS
- JavaScript
- XAMPP
- Documenso
- Docker

---

## Gestion des signatures

La convention comporte 5 emplacements de signature :

1. Chef d'établissement
2. Représentant de l'entreprise
3. Élève ou représentant légal
4. Enseignant référent
5. Tuteur en entreprise

---

## État du projet

- [x] Création de la base de données
- [x] Création de la table `signatures`
- [x] Connexion PHP → MySQL
- [x] Création de la page d'accueil
- [x] Création de l'espace élève
- [x] Création de la page de connexion élève
- [ ] Étude complète d'ESUP-Stage
- [ ] Installation/test d'ESUP-Stage
- [ ] Étude de Documenso
- [ ] Intégration de la signature électronique
- [ ] Gestion des conventions
- [ ] Gestion des signatures
- [ ] Espace personnel
- [ ] Espace entreprise
- [ ] Tests
- [ ] Documentation finale
