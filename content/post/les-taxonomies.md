---
title: "12. Les Taxonomies"
date: 2018-10-15T11:21:33+02:00
draft: false
description: "La classification du contenu."
img: ""
author: "Maxime"
---

# Qu'est-ce que c'est ?

Les Taxonomies nous permettent de classer notre contenu. 

Par exemple, si vous avez un blog sur la nourriture et que vous avez écrit des articles dans lesquels il y a des recettes, vous pouvez indiquer que ces articles appartiennent à la catégorie recettes et une fois que vous faites une recherche via une catégorie, vous retrouvez l'ensemble des articles concernés.

# Démonstration

Par défaut, Hugo contient deux taxonomies : `tags` et `categories`.

Créez un nouveau fichier `i.md` au même niveau que `a.md` et `g.md`.

Modifiez les frontmatter de `a.md`, `g.md` et `i.md` en ajoutant ces lignes :

**a.md**
```
tags: ["tag1", "tag2", "tag3"]
categories: ["category1"]
```

**g.md**

```
tags: ["tag2", "tag3"]
categories: ["category2"]
```

**i.md**

```
tags: ["tag3"]
categories: ["category1"]
```

Les tags sont un peu comme des mots clés et tandis que les catégories sont considérés comme...des catégories !

Les `[]` sont l'équivalent d'un tableau, de ce fait nous pouvons donner plus mots clés ou catégories à notre contenu.

Grâce à notre thème, vous pouvez voir que de nouvelles choses sont apparus au niveau des pages A, G et I. 

Et si vous cliquez sur une catégorie ou un tag, cela vous emmènera sur une page liste où seule les pages concernées par le tag ou la catégorie s'afficheront. C'est la magie d'Hugo !

# Peut-on créer nos propres Taxonomies ?

Oui ! Mais il faudra indiquer à Hugo que c'est une nouvelle taxonomy, sinon il ne vous créera pas de page liste appropriée.

Par exemple, on va créer une taxonomy qui s'appelle `moods` :

**Dans le frontmatter de `a.md`**

```
moods: ["Happy", "Sad"]
```

Pour dire à Hugo que `moods` est une nouvelle taxonomy, nous allons devoir modifier le fichier `config.toml` en ajoutant :

```
[taxonomies]
    tag = "tags"
    category = "categories"
    mood = "moods" 
```

La syntaxe est la suivante, vous indiquez d'abord le singulier et ensuite le pluriel (le pluriel est le mot que vous utiliserez dans vos frontmatter).

Il est impératif de réécrire les taxonomies par défaut d'Hugo pour que la nouvelle soit prise en compte.









