---
title: "22. Le dossier partials"
date: 2018-10-19T10:18:21+02:00
draft: false
description: "L'art de couper ses modèles en plusieurs parties."
img: ""
author: "Maxime"
---

# Où se trouve le dossier partials et que contient-il ?

Le dossier partials est un dossier qui se créé dans le dossier `\layouts`. Il contient les différentes parties de vos modèles.

Par exemple, si vous le souhaitez vous pouvez couper votre page d'accueil en plusieurs partie : en-tête, menu, section, pied de page. Vous vous retrouvez avec un fichier pour chaque partie, ce qui permet d'avoir une organisation plus efficace, et ensuite vous n'avez plus qu'à injecter le tout dans votre fichier d'index.

# Mieux vaut un exemple

Créez le dossier `\partials` dans le dossier `\layouts`.

Ensuite, créez un fichier `header.html` dans le dossier `\partials` et ajoutez-y le contenu suivant :

```
<h1>Ici se trouve le titre du fichier header.html</h1>
<h2>{{ .Date }}</h2>
<h3>Créé par {{ .Params.author }}</h3>
<hr>
```

Maintenant nous allons injecter le contenu de ce fichier dans `single.html` :

```
{{ partial "header.html" . }}

<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>

{{ range .Site.Data.films }}
	<p>
		{{ .nom }} ({{ .annee }})<br>
		De {{ .realisateur }} ({{ .pays }})<br>
	</p>
{{ end }}
```

Pour l'injecter nous utiliser le tag `{{ partial "nomDuFichier" . }}`. Le "." permet d'accéder à toutes les variables du fichier.
