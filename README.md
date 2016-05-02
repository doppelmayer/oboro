# oboro
Projet transmédia

## Technologies utilisées
Le projet se base sur la distibution de fichiers HTML, nous utilisons un simple serveur PHP pour s'occuper de celle-ci.
Gulp et du coup nodeJS sont uitlisés pour la gestion du déploiement.

## Installation
Téléchargement du repository et des modules node
```
git clone git@github.com:simkarlier/oboro.git
npm install
```

## Déploiement
Le projet est composé de deux répertoires : src et dist. Le répertoire src est celui utilisé pour le développement et dist est une version minifiée de celui-ci utilisée pour la version production. Le script présent dans Gulpfile.js regroupe les fichiers js et css dans des fichiers uniques permettant ainsi une gestion plus facile des parties.

Après chaque changement :

Pour le développpement (compilation dans ./src)
```
gulp build --env=dev
```


Pour la production (compilation dans ./dist), copie des autres fichiers présent dans ./src
```
gulp build --env=prod
```


### Développement

## Architecture
![alt text](https://github.com/simkarlier/oboro/blob/master/doc/img/manuel_image.png "Loader")

* Un loader (dans app.js) nous permet de charger les parties dynamiquement (pendant qu'une video charge par example), ce qui permet une transition fluide entre les différentes 		scènes. (Quelques examples ci-dessous )
..* `new Part("intro")` charge par example les éléments (JS, HTML,CSS)
..* `window.appendNext("intro")` charge dans la DOM les éléments mais ne les affiche pas
..* `parts[1].show()` affiche la partie 1

* Une fonction globale `window.next()` nous permet de passer à la prochaine partie






