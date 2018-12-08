# Générateur de site statique

Ceci est un projet proposé à des étudiants en Python.

## Qu'est-ce qu'un site statique

Un site internet statique est un site composé uniquement de fichiers présents dans un dossier :

* des fichiers HTML,
* des fichiers CSS,
* des fichiers JavaScript,
* des images,
* des vidéos,
* …

Cela s'oppose aux sites internet dynamique, où certains de ces fichiers sont générés à la volée par du logiciel, à partir par exemple de données dans une base données.

## Héberger un site statique

Héberger un site dynamique est plus complexe, il faut en effet installer le logiciel qui va générer les fichiers à la volée. Par contre, héberger un site statique est relativement simple, il suffit d'avoir un petit serveur web qui met à disposition le dossier contenant les fichiers statiques.

### Github

Github fournit un hébergement gratuit de site statique. Il suffit de créer un dépôt git avec Github, et de commiter dans une branche spécifique. Votre site est alors accessible à l'adresse suivante : https://votre_login.github.io/votre_nom_de_depot/

Plus de renseignement sur :

* https://pages.github.com/
* https://www.christopheducamp.com/2013/12/21/demarrer-avec-pages-github/
* https://developer.mozilla.org/fr/docs/Apprendre/Utiliser_les_pages_GitHub
  
### Utiliser un serveur web

Des outils commes Apache ou Nginx permettent de rendre accessible votre site par internet ou intranet :k
* https://httpd.apache.org/docs/trunk/fr/getting-started.html
* http://sametmax.com/servir-des-fichiers-statiques-avec-nginx/
* https://doc.ubuntu-fr.org/nginx
* https://nginxconfig.io/

Python vous fournit un serveur web minimaliste, par exemple pour aller sur http://localhost:8080/ et y voir le site statique dont les fichiers sont dans `./dossier_de_mon_site/`.

```
python -m http.server 8080  --directory ./dossier_de_mon_site/
```

* Github
* Apache
* Nginx
* python -m http.server

## Génerer un site statique

Les fichiers compris par un navigateur internet sont aux formats HTML/CSS/JavaScript. Vous n'avez peut-être pas envie de taper du HTML quand vous écrivez un blog. Il serait pratique de générer les pages web à partir d'un format textuel simple, comme le markdown (https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf), langage utilisé pour écrire le document que vous lisez actuellement.

## Projet

Vous allez réaliser un outil convertissant un dossier de fichiers markdown et d'images en un autre dossier contenant les fichiers d'un site statique. Du HTML sera généré à partir du markdown, et cet HTML sera mélangé avec des modèles de pages web pour générer des pages toutes conformes au même modèle (par exemple avec le même logo, le même sommaire de site internet, le même fichier CSS référencé…)

### Réalisation d'une interface en ligne de commande

Vous allez réaliser un outil en ligne de commande. Il prendra au moins comme paramètres :

* le chemin du dossier de fichiers
* le chemin du dossier où seront mis les fichiers générés
* éventuellement le dossier contenant des modèles de pages web à compléter
* de l'aide pour exliquer les paramètres de la commande

Vous pouvez utiliser :

* sys.argv (mais je ne vous le conseille pas)
* argparse (https://docs.python.org/fr/3/howto/argparse.html)
* click (https://click.palletsprojects.com/en/7.x/)

### Conversion de markdown vers HTML


### Rendu sur Github

### Projet open-source
