---
title: "18. Les Fonctions"
date: 2018-10-17T13:34:57+02:00
draft: false
description: ""
img: ""
author: "Maxime"
---

# A quoi servent-elles ?

Hugo contient des fonctions déjà programmées qui permettent de faire certaines choses pour nous aider dans notre projet de création de site internet.

Vous pouvez trouver la liste des fonctions <a href="https://gohugo.io/functions/">ici</a>.


# Utilisation

Elles ne s'utilisent uniquement dans les modèles, soit dans le dossier `\layouts`. Et nous les appelons de cette manière :

```
{{ nomDeLaFonction param2 param1 }}
```

Chaque fonction utilise un certain nombre de paramètres.

Par exemple la fonction `add` prend deux nombres en paramètre et les additionne :

```
{{ add 4 5 }}
```

Cela écrira "9".


# Exemple de la fonction "range"

La fonction `range` est très souvent utilisée sur les pages "Liste" pour afficher toutes les pages du dossier concerné. 

C'est une des fonctions qui s'utilise sous la forme d'un bloc, c'est à dire que nous ouvrons la fonction avec {{ range param1 }} et nous la fermons avec {{ end }}. Entre ces deux balises vous avez juste à mettre ce que vous souhaitez utiliser, et généralement vous allez faire appelle à des variables.

- Notre fichier `list.html` :

```
<h1>Page Liste</h1>
	{{ range .Pages }}
		<a href="{{ .URL }}">{{ .Title }}</a><br/>
	{{ end }}
```

Ici la fonction `range` va parcourir le dossier `\content` et afficher le titre de chaque page sous la forme d'un lien.

**Résultat :**

<img src="/img/post/les-fonctions-1.png" alt="" style="width: 100%;" />
