---
title: "4. La structure d'Hugo"
date: 2018-10-11T10:58:18+02:00
draft: false
description: "L'organisation des dossiers."
img: ""
author: "Maxime"
---

# Le tour des dossiers

Maintenant que votre site a été créé, vous pouvez voir qu'il contient plusieurs dossiers :

<img src="/img/post/structure-dossier-1.png" alt="" style="width:100%;" />

On va faire un petit tour rapide de ceux-ci.

**Le dossier `\archetypes`**

Si vous êtes débutant vous n'utiliserez pas beaucoup ce dossier mais en gros il sert à définir des valeurs par défaut du contenu que vous créez.

Par exemple, lorsque vous avez l'intention de créer des articles, vous pouvez leur donner en valeur par défaut un titre, une date, une catégorie, etc. Ces valeurs seront ensuite attribuées à chaque article au moment de leur création.

**Le dossier `\content`**

C'est là où vivra le contenu rédactionnel de votre site. Vous pourrez créer des dossiers (des sections) à l'intérieur de celui-ci pour mieux organiser votre contenu (articles, blog, etc.).

**Le dossier `\data`**

Ce répertoire est utilisé pour stocker des fichiers de configuration ou des modèles de données (un peu comme les bases de données) pouvant être utilisés par Hugo. Ces fichiers seront écrit au format YAML, JSON ou TOML. Rien de bien compliqué, vous verrez.

**Le dossier `\layouts`**

Ici vous y trouverez des fichiers au format ```.html```, si vous avez un peu de connaissances dans ce langage, c'est ici que vous pourrez modifier les vues (ce que vous voyez à l'écran) et changer la structure du site.

**Le dossier `\static`**

Dossier très important. C'est l'endroit où vous stockez tous les fichiers statiques de votre site. C'est-à-dire tout ce qui ne change pas d'une page à l'autre, donc nous avons les images, les fichiers de style en format ```.css``` ou encore des fichiers en langage ```javascript```.

**Le dossier `\themes`**

Si vous êtes un AS d'Hugo, d'HTML et de CSS vous pouvez créer votre propre thème ici. Sinon il faut savoir qu'Hugo est génial car il propose une bibliothèque de thème déjà pré-construit que l'on a plus qu'à télécharger et adapter à nos besoins (un peu comme les CMS tel que WordPress, Joomla, etc.).

**Le fichier `config.toml`**

C'est le fichier de configuration principal de votre site (il peut aussi être au format ```.yml``` ou ```.json```).

Par défaut, vous y trouverez : 

```
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
```

Vous pouvez voir que c'est ici que vous donnerez le titre de votre site, le langage dans lequel il est écrit, l'adresse de base de votre site, et vous pourrez mettre plein d'autres choses.
