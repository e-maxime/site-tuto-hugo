---
title: "11. Les Shortcodes"
date: 2018-10-12T11:14:27+02:00
draft: false
description: "Images, vidéos, Tweets, etc."
img: ""
author: "Maxime"
---

# Qu-est-ce que les Shortcodes ?

Les Shortcodes sont des petits bouts de code qui vont vous permettre d'intégrer assez facilement des éléments tel que des vidéos, images, des photos Instagram, et bien d'autres encore.
Nous pourrions très bien utiliser des balises HTML, c'est tout à fait faisable, mais si vous n'êtes pas à l'aise avec l'HTML alors les Shortcodes sont fais pour vous.

# Intégration d'une vidéo

Nous allons intégrer une vidéo YouTube dans notre fichier `a.md`

Pour cela, nous avons besoin du shortcode &lt;youtube> et de l'identifiant de la vidéo que vous pouvez trouver ici (surligné en bleu) :

<img src="/img/post/shortcodes-1.png" alt="" style="width: 100%;" />

Dans votre fichier `a.md`, ajoutez :

```
{{</* youtube qtIqKaDlqXo */>}}
```

Dirigez-vous sur la page A et vous obtenez :

<img src="/img/post/shortcodes-2.png" alt="" style="width: 100%;" />
<br/><br/><br/>
Plus tard vous pourrez créer, si vous le souhaitez, vos propres shortcodes, en attendant vous pouvez retrouver une liste déjà conçu sur la documentation d'Hugo <a href="https://gohugo.io/content-management/shortcodes/">ici</a>.