---
title: "16. Aller plus loin dans la structure des modèles"
date: 2018-10-16T11:30:20+02:00
draft: false
description: "La puissance d'Hugo pour structurer ses modèles."
img: ""
author: "Maxime"
---

# Les modèles de bases

Afin de mieux structurer vos modèles il existe les modèles de bases dont on nomme le fichier `baseof.html`.

Concrètement dans un fichier vous avez une structure définie, vous pouvez la définir par défaut dans le fichier `baseof.html` et par la suite dans vos fichiers `list.html` et `single.html` vous n'aurez plus qu'à modifier la partie qui doit être modifiée.

# Un peu de pratique

Nous allons travailler dans le dossier `\layouts\_default` dans lequel nous avons les fichiers `list.html` et `single.html` vierges.

**Créez un fichier `baseof.html`**

Mettez-y ceci :

```
<!DOCTYPE html>
<html>
<head>
	<title>Titre</title>
</head>
<body>
	Haut de baseof.html
	<hr>
	{{ block "main" . }}

	{{ end }}
	<hr>
	Bas de baseof.html
</body>
</html>
```

- `{{ block "main" . }} et {{ end }}` détermine un bloc que l'on appelle "main" dans lequel nous pourrons mettre un contenu adapté à la page. Le "`.`" signifie que nous voulons accéder à toutes les variables disponibles (nous en parlerons dans un prochain chapitre). Ce qui entoure ce bloc restera inchangé lors du parcours des pages.

**Modifier le bloc "main" dans les pages "Liste" et "Simple"**

**`list.html`**

```
{{ define "main" }}
    Ceci est la page liste
{{ end }}
```

Dirigez-vous sur `localhost:1313` :

<img src="/img/post/aller-plus-loin-structure-modeles-1.png" alt="" style="width: 100%;" />

**`single.html`**

```
{{ define "main" }}
    Ceci est la page simple
{{ end }}
```

Dirigez-vous sur `localhost:1313/a` :

<img src="/img/post/aller-plus-loin-structure-modeles-2.png" alt="" style="width: 100%;" />

Vous pouvez voir que seul le contenu qui se trouve au milieu change car ce qui l'entoure est défini par défaut dans `baseof.html`.

**Encore un peu**

`baseof.html` :

```
<!DOCTYPE html>
<html>
<head>
	<title>Titre</title>
</head>
<body>
	Haut de baseof.html
	<hr>
	{{ block "main" . }}

	{{ end }}
    <br>
	{{ block "section" .}}
		Ceci est le bloc section par défaut
	{{ end }}
	<hr>
	Bas de baseof.html
</body>
</html>
```

Dirigez-vous sur `localhost:1313` :

<img src="/img/post/aller-plus-loin-structure-modeles-3.png" alt="" style="width: 100%;" />

`single.html` :

```
{{ define "main" }}
	Ceci est la page simple
{{ end }}

{{ define "section" }}
	Ceci est le bloc section de la page simple
{{ end }}
```

Dirigez-vous sur `localhost:1313/a` :

<img src="/img/post/aller-plus-loin-structure-modeles-4.png" alt="" style="width: 100%;" />
