---
title: "6. Créer du contenu"
date: 2018-10-11T14:04:29+02:00
draft: false
description: "Les vraies choses commencent !"
img: ""
author: "Maxime"
---

Si vous l'avez bien deviné, dans ce chapitre, nous allons passer un peu de temps dans le dossier `\content`.

Pour créer du contenu nous allons passer par l'invite de commande/Terminal. Faites bien attention à être dans le bon dossier avant d'exécuter les commandes qui vont suivre.

# Créer le premier fichier

Pour créer votre premier fichier de contenu, tapez la commande `hugo new a.md` :
```
C:\wamp64\www\test-site>hugo new a.md
C:\wamp64\www\test-site\content\a.md created
```

Un fichier `a` sera créé avec l'extension `.md` qui signifie `markdown`, c'est un langage de balisage facile à lire et à écrire.

Vous avez votre premier fichier `a.md` qui contient :

<img src="/img/post/creer-contenu-1.png" alt="" style="width:100%;" />

Ce que vous voyez entre les `---` s'appelle le `frontmatter`, ce sont tout simplement les paramètres de votre fichier. <br/>
Vous pouvez changer ces paramètres manuellement ou bien créer un fichier dans le dossier `\archetypes` qui permettra d'établir des paramètres par défaut mais nous verrons ça plus tard.

Nous avons donc ici en paramètre, le titre du fichier, la date de publication et l'option brouillon.

# Rédaction du contenu

Vous pouvez maintenant mettre le contenu que vous souhaitez en dessous des `---` :

<img src="/img/post/creer-contenu-2.png" alt="" style="width:100%;" />

# Créer un fichier dans un dossier

Pour organiser votre contenu, cela vous arrivera tout le temps de créer plusieurs dossiers dans le dossier `\content`. Et pour s'organiser dès le début, vous pouvez directement tapez la commande `hugo new dossier1/b.md` :

```
C:\wamp64\www\test-site>hugo new dossier1/b.md
C:\wamp64\www\test-site\content\dossier1\b.md created
```

<img src="/img/post/creer-contenu-3.png" alt="" style="width:100%;" />

Pour vérifier que tout fonctionne tapez la commande :

```
hugo server -D
```

Le `-D` signifie qu'il doit afficher le contenu où l'option brouillon est activée (`draft = "true"`).

Vous devriez obtenir ceci :

<img src="/img/post/creer-contenu-4.png" alt="" style="width:100%;" />
