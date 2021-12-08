## @showdialog

Crée l'animation d'un battement de coeur lorsque le micro:bit est secoué.

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer l'icône ||`` dans le bloc ``||input: lorsque secouer||``.

Choisis l'icône du grand coeur.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
})

```

## Étape 3

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| basic: montrer l'icône ||``.


```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
})

```

## Étape 4

Ajoute le bloc ``|| basic: montrer l'icône ||`` sous le bloc ``|| basic: pause (ms) 100 ||``.

Choisis l'icône du petit coeur.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
    basic.showIcon(IconNames.SmallHeart)
})

```

## Étape 5

Ajoute le bloc ``|| basic: pause (ms) 100 ||`` sous le bloc ``|| basic: montrer l'icône ||``.


```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(100)
    basic.showIcon(IconNames.SmallHeart)
    basic.pause(100)
})

```

## Étape 6

Fais répéter 2 fois l'animation.

Ajoute le bloc ``|| loops: Répéter 2 fois ||`` dans la séquence de programmation.


```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
        basic.showIcon(IconNames.Heart)
        basic.pause(100)
        basic.showIcon(IconNames.SmallHeart)
        basic.pause(100)
    }
})

```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le programme!