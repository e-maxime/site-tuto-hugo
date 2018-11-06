---
title: "20. Les Conditions (suite)"
date: 2018-10-17T15:11:41+02:00
draft: false
description: ""
img: ""
author: "Maxime"
---

# Quelques exemples en plus

Nous avons vu quelles opérations nous pouvons faire, je les rappelle :

- eq : égale
- lt : plus petit que
- le : plus petit que ou égale à
- gt : plus grand que
- ge : plus grand que ou égale à

Vous pouvez garder ce que vous avez dans vos fichiers, nous allons sauter quelques lignes pour voir des exemples.

### Egale ou pas égale

`single.html`

```
...

<br><br><br>

<h1>
	{{ if eq "rouge" "bleu" }}
		Le rouge c'est du rouge
	{{ else }}
		Le rouge ce n'est pas du bleu
	{{ end }}
</h1>

<h1>
	{{ if not (eq "rouge" "bleu") }}
		Le rouge c'est du rouge
	{{ else }}
		Le rouge ce n'est pas du bleu
	{{ end }}
</h1>
```

Le premier regarde si les deux valeurs sont égales, le deuxième regarde si les valeurs ne sont pas égales.


### lt, le, gt, ge

Un exemple suffira, le principe est le même pour tous, ajoutez :

`single.html`

```
...

<h1>
	{{ if gt 5 7 }}
		5 est plus grand que 7
	{{ else if lt 5 7 }}
		5 est plus petit que 7
	{{ else }}
		5 est égal à 7
	{{ end }}
</h1>
```

## Ajout de and ou or

Nous pouvons aussi vérifier plusieurs choses :

`single.html`

```
...

<h1>
	{{ if and (gt 5 7) (le 1 6) }}
		5 est plus grand que 7 ET 1 est plus petit ou égal à 6
	{{ else }}
		Les conditions ne sont pas bonnes
	{{ end }}
</h1>

<h1>
	{{ if or (gt 5 7) (le 1 6) }}
		5 n'est pas plus grand que 7 mais 1 est plus petit ou égal à 6
	{{ else }}
		Les conditions ne sont pas bonnes
	{{ end }}
</h1>
```

Lorsque nous utilisons un "`and`" il faut que toutes les conditions soit exactent pour afficher la première réponse. Alors que l'utilisation d'un "`or`" permet de vérifier si au moins une des conditions est exacte.

Vous pouvez vérifier toutes les réponses des conditions que nous avons fait sur vos pages simples.


