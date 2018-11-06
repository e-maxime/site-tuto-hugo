---
title: "13. Modifier les pages \"Liste\""
date: 2018-10-15T13:53:01+02:00
draft: false
description: "Créer ses propres templates."
img: ""
author: "Maxime"
---

# Commençons par quelques explications

Comme vous avez pu le voir, les pages "Liste" et les pages "Simple" ont toutes le même aspect (en-tête, pied de page). Seul le contenu intérieur de la page et le titre de l'en-tête change.

Et nous allons voir ici comment créer nous-mêmes notre template (modèle) pour les pages "Liste". Le problème c'est qu'il faut s'y connaitre un peu en langage HTML donc je vous invite à aller consulter quelques tutoriels sur internet pour comprendre comment celui-ci fonctionne.

Mais avant de commencer, faites en sorte d'avoir la même architecture dans votre dossier `\content` :

<img src="/img/post/modifier-pages-liste-1.png" alt="" style="width: 100%" />

# Etape 0

Pour modifier nos modèles, nous allons intervenir dans le dossier `\layouts`. Toutefois, afin de voir comment cela fonctionne, dirigez-vous vers `\themes\ga-hugo-theme\layouts\`.

Vous y trouvez 2 dossiers :

- `\_default` qui contient nos modèles des pages Liste et Simple
- `\partials` qui contient des morceaux de pages que l'on intègre dans nos modèles mais nous n'en parlerons pas ici

Essayez de modifier le fichier `list.html` comme ceci :

```
...
<body>
     {{ partial "header" (dict "Kind" .Kind "Template" "List") }}
     {{.Content}}
        Test de réécriture sur le fichier list.html
     {{ range .Pages }}
...
```

Vous obtenez :

<img src="/img/post/modifier-pages-liste-3.png" alt="" style="width: 100%" />

Effacez ce que vous avez fait.

# Etape 1

Pour créer vos propres modèles il faut vous fier à l'architecture du thème que vous avez téléchargé.

En l'occurence dans votre dossier `\layouts` créez un dossier `\_default` puis un fichier `list.html` comme ceci :

<img src="/img/post/modifier-pages-liste-4.png" alt="" style="width: 100%" />

# Etape 2

Maintenant que votre fichier `list.html` a été créé, mettez-y un peu de texte et vous verrez que vos pages "liste" ne contiennent plus que le texte que vous avez saisi.

# Etape 3

Effacez le texte que vous avez mis et mettez-y ceci, nous allons parler de ce qu'il s'y trouve entre les balises `<body></body>` :

```
<!DOCTYPE html>
<html>
<head>
	<title>Page Liste</title>
</head>
<body>
	{{ .Content }}
	<ul>
		{{ range .Pages }}
		<li><a href="{{ .URL }}">{{ .Title }}</a></li>
		{{ end }}
	</ul>
</body>
</html>
```

- `{{ .Content }}` fait référence au contenu du dossier courant
- `{{ range .Pages }}` permet de parcourir le contenu des fichiers du dossier courant
- `{{ .URL }}` fait référence ou permet d'afficher le lien du dossier ou fichier courant
- `{{ .Title }}` affiche le titre du fichier courant
- `{{ end }}` permet d'arrêter le parcours de `{{ range }}`

Tout le reste n'est que du langage HTML.

Vous obtenez donc :

<img src="/img/post/modifier-pages-liste-5.png" alt="" style="width: 100%" />
