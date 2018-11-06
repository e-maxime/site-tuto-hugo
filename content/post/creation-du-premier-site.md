---
title: "3. Création du premier site"
date: 2018-10-11T09:59:44+02:00
draft: false
description: "C'est parti pour votre premier site avec Hugo."
img: ""
author: "Maxime"
---

# Créer le dossier pour stocker le site


- Créez un dossier où vous le souhaitez sur votre ordinateur, pour stocker votre site
- Ouvrez votre invite de commande et dirigez-vous vers l'emplacement de votre dossier, pour cela je vous donne une liste de commande qui vous seront utiles:

> **Sur Windows :**

> `cd "le nom d'un dossier"` pour rentrer dans un dossier

> `cd..` pour revenir au dossier précédent

> `dir` pour afficher le contenu du dossier

> **Sur Mac :**

> `cd "le nom d'un dossier"` pour rentrer dans un dossier

> `cd ..` pour revenir au dossier précédent

> `ls` pour afficher le contenu d'un dossier

Si le dossier que vous avez créé se trouve loin de l'emplacement où vous êtes dans votre invite de commande/Terminal, vous devrez parcourir les dossiers un à un jusqu'à y arriver.

**Exemple** :
```
cd dossier-1

cd sous-dossier-1

cd le-dossier-de-mon-site
```

- Une fois votre dossier atteint, tapez :

```
hugo new site le-nom-de-votre-site
```
Pour ma part, j'appellerai le site `test-site`.

- Vous devriez avoir ceci :

```
Congratulations! Your new Hugo site is created in C:\wamp64\www\test-site.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation.

```

