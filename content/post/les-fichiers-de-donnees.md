---
title: "21. Les fichiers de données"
date: 2018-10-19T08:38:26+02:00
draft: false
description: ""
img: ""
author: "Maxime"
---

# Les données dans un site statique

Vous utiliserez les données pour alimenter votre site, un peu comme une petite base de données.

Dans ce dossier vous pouvez mettre plusieurs type de fichier : `YAML`, `TOML` ou `JSON`.


# Pratiquons !

Dans le dossier `\data`, créez un fichier `films.json` avec pour contenu :

```
{
	"FF": {
		"nom": "Fast and Furious",
		"realisateur": "Rob Cohen",
		"pays d'origine": "Etats-Unis",
		"annee": "2001"
	},

	"HP": {
		"nom": "Harry Potter",
		"realisateur": "J. K. Rowling",
		"pays d'origine": "Etats-Unis",
		"annee": "2001"
	},

	"SDA": {
		"nom": "Le Seigneur des Anneaux",
		"realisateur": "Peter Jackson",
		"pays d'origine": "Etats-Unis",
		"annee": "2001"
	},

	"JU": {
		"nom": "Jumanji",
		"realisateur": "Jake Kasdan",
		"pays d'origine": "Etats-Unis",
		"annee": "2017"
	},

	"TKK": {
		"nom": "The Karate Kid",
		"realisateur": "Harald Zwart",
		"pays": "Etats-Unis",
		"annee": "2010"
	},

	"A2": {
		"nom": "Alad'2",
		"realisateur": "Lionel Steketee",
		"pays": "France",
		"annee": "2018"
	},

	"BCC": {
		"nom": "Bienvenue chez les Ch'tis",
		"realisateur": "Dany Boon",
		"pays": "France",
		"annee": "2008"
	},

	"AV": {
		"nom": "Avengers",
		"realisateur": "Joss Whedon",
		"pays": "Etats-Unis",
		"annee": "2012"
	},

	"LLA": {
		"nom": "Le Labyrinthe",
		"realisateur": "Wes Ball",
		"pays": "Etats-Unis",
		"annee": "2014"
	},

	"TW": {
		"nom": "Twilight",
		"realisateur": "Catherine Hardwicke",
		"pays": "Etats-Unis",
		"annee": "2009"
	},
}
```

Pour utiliser ces données nous devons parcourir le fichier et ensuite les afficher. Si vous avez bien suivi jusqu'ici, pour parcourir un fichier ou un dossier nous utilisons la fonction...`range` !

- Dans `single.html` :

```
<h1 style="color: {{ .Params.color }};">{{ .Title }}</h1>


{{ range .Site.Data.films }}
	<p>
		{{ .nom }} ({{ .annee }})<br>
		De {{ .realisateur }} ({{ .pays }})<br>
	</p>
{{ end }}
```

**Résultat :**

<img src="/img/post/fichiers-donnees-1.png" alt="" style="width: 100%;" />