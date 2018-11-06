---
title: "15. Changer les Modèles"
date: 2018-10-16T10:45:37+02:00
draft: false
description: "Créer ou modifier des modèles, un jeu d'enfant !"
img: ""
author: "Maxime"
---

# Changer le modèle de la page d'Accueil

Pour changer le template de la page d'accueil, une chose à faire : créer un fichier `index.html`.

**Où ça ?**

Rappelez-vous les modèles sont dans le dossier `\layouts`, la page d'accueil se situe à la racine de ce dossier donc vous n'avez plus qu'à créer un fichier `index.html` dans celui-ci et mettez-y ce que vous voulez.

# Changer le modèle des pages "Simple"

Hugo est composé de pages "Liste" et "Simple" dont les modèles respectifs sont `list.html` et `single.html`.

Si vous souhaitez changer l'aspect des pages "Simple" qu'il y a dans le dossier `\dossier1`, suivez ces instructions :

**Créez un dossier du même nom dans le dossier `\layouts`**

<img src="/img/post/changer-modeles-1.png" alt="" style="width: 100%;" />

**Créez un fichier `single.html` dans le dossier `\layouts\dossier1`**

<img src="/img/post/changer-modeles-2.png" alt="" style="width: 100%;" />

**Ajoutez un peu de contenu**

Par exemple :

```
<!DOCTYPE html>
<html>
<head>
	<title>{{ .Title }}</title>
</head>
<body>
	<h1>Nouveau modèle pour les pages simples</h1>
	<br>
	<h2>{{ .Title }}</h2>
	<p>{{ .Content }}</p>
</body>
</html>
```

Et le tour est joué ! Vous pouvez contempler le résultat sur `localhost:1313/a`. 

Vous pouvez faire exactement la même chose pour les pages listes en créant un fichier `list.html`.
