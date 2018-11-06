---
title: "2. Installation d'Hugo sur Mac"
date: 2018-10-10T15:39:07+02:00
draft: false
description: "Préparer le terrain sur Mac."
img: ""
author: "Maxime"
---

### Etape 1 - Installer brew  
  
- Dirigez vous sur le site <a href="https://brew.sh/">brew.sh</a>
- Suivez les intructions, copiez la ligne :

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- Collez la dans votre Terminal et appuyez sur Entrée (votre mot de passe vous sera certainement demandé)

### Etape 2 - Installer Hugo

- Dans votre Terminal, écrivez la commande :

```
brew install hugo
```

### Etape 3 - Tester l'installation

- Dans votre terminal, écrivez la commande :

```
hugo version
```

- Vous devriez avoir quelque chose qui ressemble à ceci :

```
Hugo Static Site Generator v0.46/extended darwin/amd64 BuildDate: unknown
```