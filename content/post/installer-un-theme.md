---
title: "5. Installation d'un thème"
date: 2018-10-11T11:54:20+02:00
draft: false
description: "Installer et utiliser un thème."
img: ""
author: "Maxime"
---

Pour le cours j'utiliserai un thème qui n'est pas répertorié sur le site d'Hugo mais qui permettra de manipuler simplement Hugo et sa structure. Le thème a été créé par <a href="">Mike Dane</a>, un développeur américain qui fait des tutoriaux.

Dirigez vous vers l'adresse https://github.com/giraffeacademy/ga-hugo-theme pour télécharger le thème (fichier ```.zip```) :

<img src="/img/post/installer-theme-1.png" alt="" style="width:100%;"/>

Extractez le contenu du fichier dans le dossier `\themes` de votre site.

Renommez le dossier `ga-hugo-theme-master` en `ga-hugo-theme`.

<img src="/img/post/installer-theme-2.png" alt="" style="width:100%;"/>

Ouvrez le dossier `\ga-hugo-theme`, l'intérieur ressemble à un projet Hugo.

Une dernière chose à faire pour que le thème fonctionne, ouvrez le fichier `config.toml` de votre site dans votre éditeur de texte préféré.

Et rajoutez la ligne :

```
theme = "ga-hugo-theme"
```

Pour vérifier que tout fonctionne, ouvrez votre terminal, accédez à l'emplacement de votre site et tapez la commande :

```
hugo server
```

Vous devriez avoir ceci :

```
C:\wamp64\www\test-site>hugo server
Building sites …
                   | EN
+------------------+----+
  Pages            |  3
  Paginator pages  |  0
  Non-page files   |  0
  Static files     |  0
  Processed images |  0
  Aliases          |  0
  Sitemaps         |  1
  Cleaned          |  0

Total in 9 ms
Watching for changes in C:\wamp64\www\test-site\{content,data,layouts,static}
Watching for config changes in C:\wamp64\www\test-site\config.toml
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```

Ouvrez votre navigateur et tapez l'adresse `http://localhost:1313/`, si tout est bon vous arrivez sur cette page :

<img src="/img/post/installer-theme-3.png" alt="" style="width:100%;"/>