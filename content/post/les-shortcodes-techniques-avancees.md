---
title: "23. Les Shortcodes techniques avancées"
date: 2018-10-19T11:28:53+02:00
draft: false
description: "Créer ses propres Shortcodes."
img: ""
author: "Maxime"
---

Ce chapitre expliquera comment créer ses propres Shortcodes, il pourra vous paraître un peu plus compliqué que les autres. 
<br>Si vous êtes arrivé jusque là, vous avez déjà toutes les bases d'Hugo et si vous le souhaitez vous pouvez passer directement au chapitre suivant, le dernier (mais n'hésitez pas à revenir sur celui-ci plus tard, il est aussi intéressant).

# Créer ses Shortcodes pour quoi faire ?

Les Shortcodes vous permettent d'éviter d'écrire du langage HTML dans vos fichiers de contenu (.md), lorsque vous voulez intégrer des éléments spécifiques.

Les Shortcodes personnalisés vont être créé dans un dossier qui s'appellera "shortcodes" et que nous mettrons dans le dossier `\layouts`.

Ces fichiers sont un peu comme les partials sauf qu'au lieu de les injecter dans nos modèles, nous les injecterons dans nos fichiers de contenu.

# Exemple simple

### Etape 0

Voici mon architecture :

<img src="/img/post/shortcodes-avancees-1.png" alt="" style="width: 100%;" />

Dans mon fichier `list.html` :

```
<h1>Page Liste</h1>

{{ range .Pages }}
    <a href="{{ .URL }}">{{ .Title }}</a><br/>
{{ end }}

```

Dans mon fichier `single.html` :

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>

{{ .Content }}
```


### Etape 1

Créez un dossier `shortcodes` dans le dossier `\layouts`. Ensuite créez un fichier `monshortcode.html` et mettez-y un peu de texte.


### Etape 2

Dans votre fichier `a.md`, ajoutez ceci :

```
{{</* monshortcode */>}}
```

Résultat : `localhost:1313/a/`

<img src="/img/post/shortcodes-avancees-2.png" alt="" style="width: 100%;" />


### Etape 3

Ajoutez des variables à votre shortcode, vous avez deux façons de le faire.

- Par nom :

`a.md`

```
{{</* monshortcode color="blue"*/>}}
```

`shortcode.html`

```
<p style="color:{{.Get `color`}}">Ceci est mon premier shortcode perso</p>
```

Résultat : `localhost:1313/a/`

<img src="/img/post/shortcodes-avancees-3.png" alt="" style="width: 100%;" />


- Par position :

`a.md`

```
{{</* monshortcode green */>}}
```

`shortcode.html`

```
<p style="color:{{.Get 0}}">Ceci est mon premier shortcode perso</p>
```


**Résultat :** `localhost:1313/a/`

<img src="/img/post/shortcodes-avancees-4.png" alt="" style="width: 100%;" />


# Exemple complexe

Les première étape est la même, commençons directement à l'étape 2.

### Etape 2

Dans votre fichier `a.md`, ajoutez ceci :

```
{{</* monshortcode */>}}

{{</* /monshortcode */>}}
```

### Etape 3

Mettez du texte entre ces deux tags.

```
Ce texte ne se situe pas dans les balises "shortcode" donc il n'est pas surligné.

{{</* monshortcode */>}}
	Ceci est le texte dans mes balises "shortcode", il est donc surligné en rose.
{{</* /monshortcode */>}}
```

### Etape 4

Dites à votre shortcode qu'il contiendra un bloc de quelque chose et qu'il faudra le surligner en rose.

`shortcode.html`

```
<p style="background-color: pink;">{{ .Inner }}</p>
```

**Résultat :** `localhost:1313/a/`

<img src="/img/post/shortcodes-avancees-5.png" alt="" style="width: 100%;" />



