---
title: "14. Modifier les pages \"Simple\""
date: 2018-10-15T15:01:48+02:00
draft: false
description: "Créer ses propres templates (suite)."
img: ""
author: "Maxime"
---

Nous avons modifier nos modèles pour les pages "Liste" et c'est le même principe pour les pages "Simple" !

# Etape 1

Dans votre dossier `\_default`, créez un fichier `single.html`

# Etape 2

Votre modèle pour les pages "Simple" est créé, maintenant il ne reste plus qu'à le remplir :

```
<!DOCTYPE html>
<html>
<head>
	<title>Page Simple</title>
</head>
<body>
	<h1>{{ .Title }}</h1>
		<h2>{{ .Date }}</h2>
			<p>{{ .Content }}</p>
</body>
</html>
```

- `{{ .Title }}` affiche le titre du fichier mentionné dans le frontmatter
- `{{ .Date }}` affiche la date mentionnée dans le frontmatter
- `{{ .Content }}` affiche le contenu

Résultat :

<img src="/img/post/modifier-pages-simple-1.png" alt="" style="width: 100%;" />
