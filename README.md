# Cours VueJS
Petit cours rapide sur VueJS (et WebPack)

https://vuejs.org/

![https://vuejs.org/](https://vuejs.org/images/logo.png)

## Principe

VueJS est un framework javasript, qui permet de créer une app / une web-app / un site avec une logique applicative en JS (bien qu'on puisse parfaitement la coupler avec du PHP ou quelconque autre langage serveur).

## Installation

```bash
npm i -g vue vue-cli
```
Vous installez vue (et ses options de ligne de commande) de façon globale sur votre machine.

## Package

VueJS donne la possibilité de créer un package déjà tout prêt, avec des tests unitaires et un linter JS.
De plus, il intègre automatiquement WebPack, un task-runner évolué et puissant qui permet entre autres de faire tourner un serveur local via NodeJS.

Pour créer tout ça :

```bash
vue install webpack mon-projet
npm i
```

Ensuite, il ne reste plus qu'à lancer le serveur de dev pour bosser :

```bash
npm run dev
```

Vous pouvez lancer votre navigateur et ouvrir http://localhost:8080 (par défaut).

## Web modules
La notion la plus importante ici est celle de **web modules**.

Concrêtement, ça nous permet d'importer des fichiers JS dans des fichiers js :

```javascript
var monTruc = require('truc');

// ou

import monTruc from 'truc';
```

Ainsi chaque fichier peut correspondre à un module, exploité par le reste de l'application uniquement par d'autres modules qui en ont besoin (système de dépendances).

## Fonctionnement
VueJS fonctionne sur un système de components-templates, définis dans des fichiers `.vue`.

Fichier de base (index.html) :

```html
<body>
	<h1>Titre</h1>
	<mon-texte></mon-texte>
</body>
```

La balise `<mon-texte>` pourra être appelée par Vue pour être remplacé par un template de votre création.

Fichier de template : monTexte.vue
```html
<template>
	<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae, cupiditate quaerat rerum eveniet voluptatum. Facilis quaerat accusamus, nihil quas. Vero harum, doloremque eveniet nam, voluptates officiis! Tenetur minima voluptate quae.</p>
</template>
```

# Ressources

* https://vuejs.org/guide/
* https://www.grafikart.fr/tutoriels/vuejs/datepicker-754

## Pourquoi utiliser du CSS modulaire ? 
* [Pourquoi j'ai arrêté d'utiliser CSS](http://putaindecode.io/fr/articles/css/stop-css/) — putain de code
* [Vers les CSS Modules](http://putaindecode.io/fr/articles/css/modules/) — putain de code
