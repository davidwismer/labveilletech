+++ 
draft = false
date = 2023-01-28T01:12:18+01:00
title = "Expérimentation: BadUIBattles"
description = "Expérience avec le feed reddit 'badUIbattles', qui répertorie des interractions avec des mauvaises interfaces utilisateur."
slug = ""
authors = ["David Wismer"]
tags = []
categories = []
externalLink = ""
series = []
+++
En discutant avec un ami à moi, j'ai découvert un feed sur Reddit qui s'appelle "badUIbattles". Sur ce feed, les utilisateurs de Reddit postent toutes sortes de designs et interractions d'interfaces utilisateurs qui sont intentionnellement mauvaises. Cela m'a bien amusé et en me baladant dans le feed, j'ai été inspiré par une idée d'expérimentation.

### Expérience
Actuellement entrain de développer un site qui me servira de portfolio, j'essaie de trouver des idées d'interractions intéressantes et uniques. Mon site contient une page de contact qui est constituée d'un formulaire qu'un visiteur peut remplir avec ses coordonnées et un message qui me seront envoyés à mon adresse mail. J'ai donc pensé expérimenter avec l'interraction du bouton d'envoi de ce formulaire.

L'idée que j'avais était un bouton qui, lorsque les informations entrées dans les champs du formulaire sont soit invalides soit manquantes, ne permet pas à l'utilisateur de le cliquer et que ce soit visuellement amusant. J'ai voulu faire en sorte que le bouton fuie la souris quand on veut cliquer dessus, jusqu'à ce que les informations du formulaire soient correctes. Je me suis inspiré d'un gif que j'ai vu sur ce fameux feed "badUIbattles" où un "Impossible Button" était tout simplement incliquable par l'utilisateur.

### Solution
Au vue de la disposition des éléments sur ma page, le plus intuitif était de faire coulisser le bouton horizontallement. Il fallait simplement qu'au moment d'un hover avec la souris sur ce bouton, l'élément se translate sur l'axe x. Le site étant mis en place sur Vue.js, j'ai pu utiliser un v-bind, qui me permet de lier une variable à une propriété CSS. De là, il était simple d'ajouter un bout de code Javascript qui me permet de donner une valeur de translation en pixel au bouton et d'ajouter dans la classe CSS du bouton la variable dans une propriété:

```CSS
.submit {
    transform: translate(v-bind(translation), 0);
}
```

Pour rendre l'interraction plus "naturel" et moins monotone, j'ai décidé d'y ajouter un côté random. C'est-à-dire que le bouton à 50% de chance d'aller à gauche et 50% de chance de se d'aller à droite. J'ai tout de même pris des précautions pour que le bouton ne sorte pas de la page.

![image](/labveilletech/images/experience.gif)

### Sources
feed reddit: https://www.reddit.com/r/badUIbattles/\
page contact avec l'expérience: https://davidwismer.onrender.com/#contact