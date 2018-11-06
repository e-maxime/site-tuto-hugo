---
title: "1. Installation d'Hugo sur Windows"
date: 2018-10-10T14:46:05+02:00
draft: false
description: "Préparer le terrain sur Windows."
img: ""
author: "Maxime"
---

### Etape 1 - Créer l'emplacement

- Dirigez-vous sur l'emplacement de votre disque `C:`
- Créez un dossier "**Hugo**" et une fois dedans créez un dossier "**bin**"


### Etape 2 - Télécharger Hugo

- Allez sur la page https://github.com/gohugoio/hugo/releases (la dernière version d'Hugo est affichée en bleu tout en haut)
- Faites défiler la page et téléchargez le fichier "`hugo_0.49_Windows-32bit.zip`" ou "`hugo_0.49_Windows-64bit.zip`" en fonction de la version de Windows que vous utilisez 32bit ou 64bit (si vous ne savez pas dirigez vous vers votre menu Démarrer puis Paramètres puis Système et enfin Informations Système)
- Déplacez le fichier .zip dans le dossier bin que vous avez créé
- Extractez le contenu dans le dossier
- Vous devriez avoir 3 fichiers dont le fichier hugo.exe

### Etape 3 - Mettre à jour les variables d'environnement

- Dans la barre de recherche de Windows en bas à gauche, écrivez "**Variables d'environnement**" et cliquez sur le résultat
- Une petite fenêtre s'ouvre, cliquez maintenant sur "**Variables d'environnement**" en bas
- Dans la section variables utilisateur, cherchez la ligne "**Path**" et double-cliquez dessus
- Faites "**Nouveau**" et ajoutez la ligne `C:\Hugo\bin`
- Vous pouvez tout fermer

### Etape 4 - Vérifier si le fichier hugo.exe fonctionne

- Ouvrez l'invite de commande, pour cela aller dans la barre de recherche Windows et écrivez "**cmd**"
- Une fenêtre noir s'ouvre, tapez alors :

```
hugo version
```

- Vous devriez avoir quelque chose qui ressemble à ceci :

```
Hugo Static Site Generator v0.45 windows/amd64 BuildDate: 2018-07-22T12:10:05Z
```