+++ 
draft = false
date = 2023-01-27T02:35:59+01:00
title = "Résumé: More Real-World Uses for :has()"
description = "Résumé d'un article qui parle des nouvelles possibilités apportées par :has() en CSS"
slug = ""
authors = ["David Wismer"]
tags = []
categories = []
externalLink = ""
series = []
+++
En 2022, les différents navigateurs web ont travaillé ensemble pour améliorer le web pour les développeurs, c'est ce qu'on a appelé "Interop 2022". Durant ce processus, le langage CSS a eu le droit à de nouvelles fonctionnalités, dont une nouvelle pseudo-class ":has()" qui permet de cibler un élément qui possède un selecteur passé en paramètre dans sa portée. Au moment de la découverte de cet article, je n'ai jamais entendu parlé de cette pseudo-class.

### Avantage
Dans cet article, l'auteur nous fait part de différentes situations qu'il imagine rencontrer où cette nouvelle pseudo-class pourrait simplifier le code. Elle pourrait être utile à certains moments où le CSS d'avant cette fonctionnalité nous forçait à devoir passer par du Javascript pour assigner des styles à des éléments en dehors du composant qui va lancer un évènement. Le premier exemple est un menu de navigation qui, lors d'un clic sur un élément du menu, va changer la couleur du header de la page. La pseudo-class has permet désormais de gérer cette situation uniquement en CSS:

```CSS
header:has(.menu--open) {
  /* mettre un style au header différent si il contient un element avec la class ".menu--open" */
}
```

### Conclusion
Les différents langages de programmation que j'utilise sont constament soumis à des changements. Il est important de se renseigner sur les nouveautés apportées pour rester le plus efficace possible.

### Sources
article: https://css-tricks.com/more-real-world-uses-for-has/\
définition ":has()": https://developer.mozilla.org/fr/docs/Web/CSS/:has\
auteur: Liam Johnston