# Redux

## Architecture

[Redux](http://redux.js.org/) est donc une des implémentations de Flux. La confusion régnait jusqu'en 2015 sur l'implémentation Flux maitresse à choisir sur un projet React, il y en avait des dizaines. Dan Abramov, jeune développeur avec de l'expérience des frameworks utilisant la programmation fonctionnelle comme paradigme de base, est arrivé avec sa solution Redux et [a époustouflé tout le monde à l'époque](https://www.youtube.com/watch?v=xsSnOQynTHs). Elle utilise des concepts utilisés en masse dans Elm, tels que [l'immutabilité](https://en.wikipedia.org/wiki/Immutable_object) ou les [fonctions pures](http://www.nicoespeon.com/en/2015/01/pure-functions-javascript/) pour gérer l'état des objets.

Redux est basé sur des [reducers](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Objets_globaux/Array/reduce) \(d'où le nom\) pour gérer les objets dans ce qui est appelé l'état en Redux \(state\). Il ne modifie pas un objet mais utilise des fonctions pures pour créer un nouvel objet et l'ajouter à l'état. Il utilise aussi un seul store, divisé par plusieurs reducers.

Alors qu'est-ce qu'un reducer ? Pour répondre, il faut déjà parler des fonctions pures. C'est un concept de programmation fonctionnelle : ce sont des fonctions qui avec les mêmes paramètres renvoient toujours la même réponse. Ce devrait être le principe de toute fonction en fait.

Parfois, des fonctions deviennent des fourre-tout, avec beaucoup de conditions, longues et peu lisibles, donc sources potentielles de bugs et difficiles à tester. Les fonctions pures sont courtes et ne font qu'une chose : renvoyer la même réponse selon un contexte donné. Un très bon article à ce sujet : [http://www.nicoespeon.com/fr/2015/01/fonctions-pures-javascript/](http://www.nicoespeon.com/fr/2015/01/fonctions-pures-javascript/)

Un reducer devrait donc être une fonction pure, dans la théorie Redux. La librairie Immutable.js n'est pas obligatoire mais convient bien à un projet de ce genre.

Il est temps d'installer les packages nécessaires :

`npm i immutable react-redux@4.4.5 redux@3.5.2 redux-form@5.2.5 --save`

Pour ceux qui démarrerait un projet from scratch, il suffit de prendre le fichier package.json des sources finales et de faire un `npm install`

## Sujet de l'application

La plupart des tutoriels présentant Redux le font dans le cadre d'une appli de "to-do", de gestion de tâches.

Le sujet de notre appli sera différent, ce sera la gestion d'une classe numérique. Notre application va permettre de gérer, très basiquement, une liste d'étudiants.

Le prochain billet détaillera la mise en place de Redux dans notre fichier app.js.

