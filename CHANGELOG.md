# Changelog

Un suivi à jour des modifications apportées à ce projet (cf [Keep a Changelog](https://keepachangelog.com/en/1.0.0/))

## A venir

Des pistes dans [README#idées](README#idées)

## [0.5.0] - en cours

### Ajouté

### Modifié

## [0.4.0] - 2020-03-27

### Ajouté

- [Frontend] Affiche un message légèrement aléatoire pour chaque réponse correcte
- [Frontend] Une page Catégories avec la liste des catégories
- [Frontend] Une page Catégorie avec la liste des questions pour la catégorie donnée
- [Frontend] Ajout de la librarie CSS Bootstrap. Cleanup du CSS.
- [Frontend] Ajout d'un "footer" avec des liens vers les autres pages
- [Frontend] Page de contribution
- [Frontend] Refactoring des components et du routing Vue.js

### Modifié

- [Data] Ajout d'un maximum d'images aux questions existantes
- [Frontend] Refonte de la page principale

## [0.3.0] - 2020-03-22

### Ajouté

- [Backend] Ajout d'un champs `answer_image_link` dans le modèle Question
- [Frontend] Une page Stats pour afficher quelques les chiffres basiques de l'application (nombre de questions, nombre de réponses, ...)
- [Frontend] Un bouton "Autre question dans la même catégorie"
- [Frontend] Affiche l'auteur et les statistiques de la question (dans la réponse)

### Modifié

- [DevOps] Ajout de la commande loaddata au Procfile
- [Frontend] Typo dans la description de l'application

## [0.2.0] - 2020-03-11

### Ajouté

- [Data] Ajout de toutes les questions (80+)
- [Backend] Un modèle QuestionStats pour commencer à avoir des stats d'usage (nombre de réponses par question, nombre de réponses correctes par question, ...)
- [Backend] Ajout d'un champs `author` dans le modèle Question
- [Backend] Ajout d'un champs `publish` (boolean) dans le modèle Question
- [Backend] Une ressource API `/questions/:id/stats` pour récupérer les résultats de chaque réponse
- [Frontend] Amélioration des champs meta dans le `<head>` de l'application, et ajout d'une image
- [Frontend] Le titre de la page (i.e. le nom de l'onglet) est maintenant un peu dynamique
- [Frontend] Ajout d'un favicon (i.e. le logo de l'onglet)
- [DevOps] Ajout du projet à [Kaffeine](https://kaffeine.herokuapp.com/) pour eviter que l'app backend se mette en pause (car elle tourne sur le plan gratuit Heroku)
- [Documentation] Ajout de la section `Idées` dans le README

### Modifié

- [Frontend] Meilleur affichage de la catégorie et de la difficulté des questions
- [Frontend] Ajout d'informations dans la page `/a-propos`

## [0.1.0] - 2020-03-08

### Ajouté

- [Data] 10 questions dans la base de donnée
- [Backend] Un modèle Question pour stocker les questions à choix multiples
- [Backend] Une ressource API `/questions` pour récupérer toutes les questions
- [Backend] Une ressource API `/questions/:id` pour récupérer une question par id
- [Backend] Une ressource API `/questions/random` pour récupérer une question au hasard
- [Backend] Chaque question possède 1 seul catégorie
- [Backend] Une console admin fournie par Django
- [Backend] Les questions sont écrites dans un fichier YAML avant d'être loadés en base de donnée
- [Frontend] Une page principale avec l'ensemble des questions, avec un filtre simple par catégorie
- [Frontend] Une page par question, avec la possibilité d'y répondre et de voir ensuite la réponse
- [Frontend] Un début de page A propos avec un lien vers le repo Github
- [DevOps] Séparation des variables d'environment (local & prod)
- [DevOps] Déploiement du Backend (Django API & Admin) sur Heroku
- [DevOps] Déploiement du Frontend (Vuejs) sur Netlify
- [Documentation] Un fichier README
- [Documentation] Un fichier CHANGELOG
