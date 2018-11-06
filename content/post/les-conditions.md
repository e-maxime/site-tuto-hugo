---
title: "19. Les Conditions"
date: 2018-10-17T14:29:48+02:00
draft: false
description: ""
img: ""
author: "Maxime"
---

# Si, sinon si, sinon...

Lorsque vous créez votre site, vous pouvez faire certaines choses sous certaines conditions.

Nous utiliserons les tags {{ if condition }}, {{ else if condition }} et {{ else }} (si, sinon si, sinon).

Dans ces tags nous pouvons faire des vérifications avec les conditions :

- eq : égale
- lt : plus petit que
- le : plus petit que ou égale à
- gt : plus grand que
- ge : plus grand que ou égale à

# Rien ne vaut un cas concret

Dans un premier temps, faites en sorte d'avoir cette architecture :

<img src="/img/post/les-conditions-1.png" alt="" style="width: 100%;" />

Ensuite dans votre fichier `single.html` :

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>

{{ range .Site.Pages }}
		<a href="{{ .URL }}">{{ .Title }}</a><br/>
{{ end }}
```

Lorsque vous serez sur les pages A, B ou C, cela vous affichera toutes les pages de votre site et en fera des liens.

### Ce que nous allons faire

Lorsque nous serons sur une page par exemple la page A, nous ferons en sorte que le lien soit de couleur vert et écrit plus gros.

`single.html`

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>

{{ $titre := .Title }}

{{ range .Site.Pages }}
		<a href="{{ .URL }}" style="{{if eq .Title $titre}}color: green; font-size: 2em;{{end}}">{{ .Title }}</a><br/>
{{ end }}
```

**Explications**

- `{{ $titre := .Title }}` permet de stocker le titre de la page que l'on voit dans une variable
- `{{ range .Site.Pages }}{{ end }}` liste toutes les pages du site
- `style="{{if eq .Title $titre}}color: green; font-size: 2em;{{end}}"` la condition qui nous dit : "Si le titre de la liste est le même que celui stocké dans la variable $titre alors je l'écris en vert et en plus gros".

**Résultat :**

`localhost:1313/a`

<img src="/img/post/les-conditions-2.png" alt="" style="width: 100%;" />

Cela vous donnera le même résultat adapté pour les pages B et C.