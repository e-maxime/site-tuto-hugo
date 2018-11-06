---
title: "17. Les Variables"
date: 2018-10-17T10:20:33+02:00
draft: false
description: ""
img: ""
author: "Maxime"
---

# Les variables, qu'est-ce que c'est ?

Les variables sont des valeurs modifiables que nous attribuons à certaines choses pour nous faciliter la tâche.

Les variables que nous utiliserons ici ne pourrons être utilisées uniquement dans nos modèles, c'est-à-dire dans les fichiers de notre dossier `\layouts`.

Et ces variables seront créées soit dans nos fichiers de contenu, dans le dossier `\content`, ou alors directement dans nos modèles.


# Combien en existent-elles ?

Hugo contient des variables par défaut que l'on a déjà utilisé tel que `.Title`, `.Date` et `.Content`. Vous pouvez retrouver une liste des variables dans la <a href="https://gohugo.io/variables/">documentation d'Hugo</a>.

Mais vous pouvez aussi créer vos propres variables.


# Comment les utilise-t-on ?

Les variables qui sont déjà contenu dans Hugo s'utilise avec des accolades comme ceci :

```
{{ .Title }}
```

Mais les variables que nous créons nous mêmes s'utilisent d'une manière différente :

```
{{ .Params.leNomDeMaVariable }}
```


# Les variables dans les fichiers de contenu

Les variables sont définis dans le frontmatter. Nous allons créer une variable de couleur que nous utiliserons pour modifier la couleur des titres en fonction de la page sur laquelle on se trouve.

Avant toute chose, faites en sorte d'avoir la même architecture :

<img src="/img/post/les-variables-1.png" alt="" style="width: 100%;" />

### Créer les variables

Dans le fichier `a.md`, ajoutez dans le frontmatter :

```
color: "blue"
```

Dans le fichier `b.md`, ajoutez dans le frontmatter :

```
color: "red"
```

Dans le fichier `c.md`, ajoutez dans le frontmatter :

```
color: "green"
```

### Utiliser les variables

- `list.html` :

```
<h1>Page Liste</h1>
<ul>
	{{ range .Pages }}
		<li><a href="{{ .URL }}">{{ .Title }}</a></li>
	{{ end }}
</ul>
```

- `single.html` avec l'utilisation de notre variable de couleur :

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>
```

**Résultat :**

<img src="/img/post/les-variables-2.png" alt="" style="width: 100%;" />
<img src="/img/post/les-variables-3.png" alt="" style="width: 100%;" />
<img src="/img/post/les-variables-4.png" alt="" style="width: 100%;" />

# Les variables dans les modèles

Vous pouvez aussi créer des variables directement dans les modèles, elles s'écrivent comme ceci :

- Si c'est une variable qui contient du texte :

```
{{ $maVariable := "leTexteQueContientLaVariable" }}
```

- Si c'est une variable qui contient un nombre :

```
{{ $maVariable := 1234 }}
```

- Si c'est une variable qui contient une valeur booléenne (vrai ou faux) :

```
{{ $maVariable := true }}
```
<br>
### Utilisation

- Dans `single.html` :

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>

{{ $prenom := "Hugo" }}

<h3>Bonjour je m'appelle {{ $prenom }}</h3>
```

**Résultat :**

<img src="/img/post/les-variables-5.png" alt="" style="width: 100%;" />






