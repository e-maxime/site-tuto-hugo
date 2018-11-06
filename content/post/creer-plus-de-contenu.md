---
title: "8. Créer plus de contenu"
date: 2018-10-11T15:39:54+02:00
draft: false
description: "Et on continu ! Encore plus de contenu !"
img: ""
author: "Maxime"
---

En vous aidant du chapitre sur la création de contenu, essayez d'obtenir cette architecture :

<img src="/img/post/creer-plus-contenu-1.png" alt="" style="width: 100%;" />

**Ce qu'on peut voir maintenant**

Les dossiers qui sont créés au "niveau 1" du dossier `\content` ont automatiquement des pages listes qui sont créés, pour le vérifier dirigez-vous sur l'adresse `http://localhost:1313/dossier1/`, cela vous affichera toutes les pages qui se trouvent dans le `\dossier1` :

<img src="/img/post/creer-plus-contenu-2.png" alt="" style="width: 100%;" />

Toutefois, à partir des dossiers de "niveau 2", les pages listes ne sont plus créées automatiquement, si vous allez sur la page `localhost:1313/dossier1/dossier2/`, vous obtiendrez une page blanche.

**Pourquoi ?**

C'est le fonctionnement par défaut d'Hugo.

Et pour avoir une page liste à partir des dossiers de "niveau 2", vous devez le faire manuellement en créant un fichier `_index.md` dans le dossier concerné.

Ici :

```
hugo new dossier1/dossier2/_index.md
```

Retournez sur la page `localhost:1313/dossier1/dossier2/` et voilà le travail :

<img src="/img/post/creer-plus-contenu-3.png" alt="" style="width: 100%;" />

**Une dernière chose**

Les pages listes affichent toutes les pages que contient le dossier concerné. Est-ce qu'on peut afficher d'autres éléments ?

Allez dans votre fichier `_index.md` que vous avez créé dans votre `\dossier2` et mettez-y un peu de contenu.

Lancez la page `localhost:1313/dossier1/dossier2/` et appréciez :

<img src="/img/post/creer-plus-contenu-4.png" alt="" style="width: 100%;" />

Vous pouvez faire la même chose dans chaque dossier en créant un fichier qui a pour nom `_index.md`.