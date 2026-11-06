# Challenge - Inspection et Analyse d'un Repository GIT

## Consignes générales

Ce challenge a pour but d'évaluer votre capacité à **explorer, comprendre et analyser l'historique d'un projet GIT**.

### Règles

- **Aucune interface graphique n'est autorisée**, vous devez travailler **exclusivement en ligne de commande** (sauf pour le FORK depuis Github)
- **L'utilisation d'outils d'intelligence artificielle est strictement interdite.**
- Vous pouvez utiliser la documentation à l'adresse suivante: https://git-scm.com/book/fr/v2
- **Objectif : comprendre l'évolution du code et reconstituer les décisions prises.**

## Travail à effectuer

Le dépôt d'origine à utiliser est disponible à l'adresse suivante :
```bash
https://github.com/ETML-RRY/324_inspection_git.git
```

### Partie 1 - Préparation

1. Faites un *FORK* du dépôt sur votre compte GitHub (Attention il faut copier toutes les branches donc il faut **décocher** la case "Copy the main branch only" sur l'interface de Github)
2. Ajoutez votre enseignant comme collaborateur à votre dépôt forké.
3. Vous trouverez une réplique de ces instructions dans le fichier README.md de votre dépôt.
4. Répondez directement aux questions dans le fichier README.md qui est au format **Markdown**
5. Pour chaque points, veuillez noter la ou les commandes `git` utilisées vous permettant de répondre à la question.
6. Pour chaque partie, effectuez au minimum un commit et un push lorsque vous avez complété les réponses de la partie correspondante.

> Le format Markdown: [https://www.markdownguide.org/basic-syntax/](https://www.markdownguide.org/basic-syntax/)


### Partie 2 — Exploration de base

1. Combien de branches existent dans le dépôt ? Citez-les.
    il y en a 5 : main; experiment/dark-mode; feature/header; feature/login; hotfix/typo
2. Quels sont les **tags** disponibles ? A quoi correspondent-ils ?  
    il y a v0.1 pour l'initial commit avec la structure + README + docs et v0.2 pour le merge du header qui intègre la navigation
3. Quelle est la **branche principale** du projet ?
    main

### Partie 3 — Historique et commits

4. Quel est le message du **premier commit** du projet ? 
    "Initial commit: structure HTML/CSS/JS + README + docs"
5. Trouvez le commit où une **clé API** a été ajoutée par erreur. Quel est son identifiant (hash court) ?  
    bea2d1a
6. Quel commit a ensuite corrigé cette erreur ? 
    1b682c9
7. Trouvez le commit où le **titre de la page d'accueil** a été corrigé.  
    6317c07
8. Quel est le message du commit qui a **ajouté le fichier `CHANGELOG.md`** et quelle commande avez-vous utilisé ?
    ed62890 j'ai fait git log

### Partie 4 — Branches et fusions

9. Quelles branches ont été fusionnées dans `main` ?  
    feature/header; feature/login
10. Quelle branche **n'a pas été fusionnée** ? Pourquoi, selon vous ? 
    experiment/dark-mode, car c'est une expériance

### Partie 5 — Analyse du contenu

11. Quelle est la **différence principale** entre les fichiers `index.html` dans les versions `v0.1` et `v0.2` et quelle commande permet de le voir rapidement ?  
    "<header><nav><a href="/">Accueil</a> | <a href="#">Contact</a></nav></header>"
    git diff 4d28bc59eee6c8f52277bf505642a0e8e3595674 5d66c29ef71dcd9f8e91794bf4c8591a9a56823d
12. Que contient la branche `feature/login` ? 
    la page de connexion et pseudo-fonction JS
13. Dans quelle branche a été ajouté le code pour le **mode sombre** ? 
    hotfix/typo 
14. Quelle bonne pratique de sécurité est évoquée dans les commits du fichier `config.js` ?
    clé API retirée; utiliser des variables d'environnement

### Partie 6 — Réflexion

15. Pourquoi est-il important de **taguer** des versions dans un projet ?
    pour les releases
16. Que peut-on déduire du style de travail de l'équipe à partir de cet historique GIT ?  
    c'est une équipe oragnisé qui a choisi un nomage claire de chaque commit

Bonne chance, et surtout... **ne vous perdez pas dans le log !** 😉