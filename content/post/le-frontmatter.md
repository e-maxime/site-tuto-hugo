---
title: "9. Le Frontmatter"
date: 2018-10-12T09:56:38+02:00
draft: false
description: "Les paramètres de votre contenu."
img: ""
author: "Maxime"
---

Le `Frontmatter` se situe en haut de votre fichier de contenu, pour notre part entre les balises `---`.<br/>
Il peut être écrit sous 3 langages différents : `YAML`, `TOML`, `JSON`. Par défaut, Hugo utilisera `YAML`.<br/>
Ces 3 langages se ressemblent beaucoup :

**YAML**

```
---
title: "Le Frontmatter"
date: 2018-10-12T09:56:38+02:00
draft: false
description: "Les paramètres de votre contenu."
img: ""
author: "Maxime"
---
```

**TOML**

```
+++
title= "Le Frontmatter"
date= 2018-10-12T09:56:38+02:00
draft= false
description= "Les paramètres de votre contenu."
img= ""
author= "Maxime"
+++
```

**JSON**

```
{
    "title": "Le Frontmatter",
    "date": "2018-10-12T09:56:38+02:00",
    "draft": "false",
    "description": "Les paramètres de votre contenu.",
    "img": "",
    "author": "Maxime"    
}
```
<br/>
# Des informations sur votre contenu

Le `Frontmatter` vous indique certaines choses sur votre contenu, si vous allez dans le fichier `a.md`, il vous indique le titre de votre fichier, sa date de publication et si c'est un brouillon ou non.

Par la suite, vous pourrez rajouter autant d'informations que vous le souhaiterez, comme vous pouvez le voir dans les exemples ci-dessus, il suffira juste de savoir comment les afficher mais nous verrons ça plus tard.