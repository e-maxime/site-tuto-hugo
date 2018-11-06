---
title: "10. Le dossier Archetypes"
date: 2018-10-12T10:23:31+02:00
draft: false
description: "Donner des informations par défaut à votre contenu."
img: ""
author: "Maxime"
---

Dans notre cas, vous avez pu voir que lorsque nous créons un fichier de contenu, il ajoute automatiquement des informations au frontmatter (ici le titre, la date et le brouillon).

**Pourquoi ?**

Allez faire un tour dans le dossier `\archetypes`, ce dossier contient un fichier nommé `default.md` qui contient :

```
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
---
```

# Qu'est-ce que ça dit ?

**title**

Ici il nous dit qu'il va prendre le nom du fichier, enlever les "`-`" et les remplacer par des espaces et en faire un titre.

**date**

Indique la date à laquelle il est créé.

**draft**

Indique si le fichier est un brouillon ou non.

# Peut-on le modifier ?

Bien sur ! En dessous de `draft`, ajoutez la ligne :

```
author: "Hugo"
```

Cela ne modifiera pas les fichiers que vous avez déjà créé mais ajoutera un auteur à tous les prochains.

Création d'un nouveau fichier :

```
hugo new g.md
```

Contenu du frontmatter de `g.md` :

```
---
title: "G"
date: 2018-10-12T10:40:35+02:00
draft: true
author: "Hugo"
---
```

Maintenant tous vos fichiers auront pour auteur "Hugo", mais vous pouvez définir des informations de contenu (frontmatter) différentes selon les dossiers.

Dans le dossier `\archetypes`, créez un fichier qui a pour nom, le nom d'un dossier qu'il y a dans `\content`, par exemple `dossier3.md` et mettez-y en contenu :

```
---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
author: "Max"
---
```

Créez un fichier `h.md` dans `\content\dossier3` :

```
hugo new dossier3/h.md
```

Vous verrez que dans le frontmatter de `h.md`, l'auteur est bien "Max". Si vous créez un fichier dans un autre dossier que `\dossier3` l'auteur sera "Hugo".

<img src="/img/post/dossier-archetypes-1.png" alt="" style="width: 100%" />