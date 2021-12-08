## @showdialog

Roche, papier, ciseau... allumettes!

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Main||``.

Ajoute le bloc ``||variables: définir Nombre à "0"||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = 0
})

```

## Étape 3

Remplace la valeur "0" dans le bloc ``||variables: définir Main||`` par le bloc ``||math: choisir au hasard de "0" à "10"||``.

Remplace les valeurs "0" et "10" dans le bloc ``||math: choisir au hasard de "0" à "10"||`` par les valeurs "1" et "3".

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
})

```

## Étape 4

Ajoute le bloc ``||logic: si vrai alors||`` sous le bloc ``||input: lorsque secouer||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (true) {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||logic: "0" = "0"||`` dans le bloc ``||logic: si||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (0 == 0) {
    	
    }
})

```

## Étape 6

Remplace la valeur "0" du bloc ``||logic: "0" = "0"||`` par le bloc ``||variables:Main||``.

Remplace la valeur "0" du bloc ``||logic: "0" = "0"||`` par la valeur "1".

La valeur 1 représente les ciseaux.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (Main == 1) {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||basic: montrer l'icône||`` sous le bloc ``||logic: "si Main = 1"||``.

Ajoute le bloc ``||basic: pause (ms) 500||`` sous le bloc ``||basic: montrer l'icône||``.

```blocks

let Main = 0
input.onGesture(Gesture.Shake, function () {
    Main = randint(1, 3)
    if (Main == 1) {
        basic.showIcon(IconNames.Scissors)
        basic.pause(500)
    }
})

```

## @showdialog

Oups! Les étapes pour programmer la roche, le papier et les allumettes ont disparu.

Programme le micro:bit pour qu'il puisse afficher les autres éléments du jeu.

La valeur 1 représente les ``||logic: ciseaux||``. La valeur 2 représente la ``||logic: roche||``.

La valeur 3 représente le ``||logic: papier||``. La valeur 4 représente les ``||logic: allumettes||`` .

## Étape 8

Télécharge le programme dans le micro:bit.

Teste le programme avec une autre équipe!