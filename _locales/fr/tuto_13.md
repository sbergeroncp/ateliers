## @showdialog

Crée une boule de neige à l'aide du micro:bit.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer leds ||`` dans le bloc ``||basic: au démarrage||``.

Dessine une boule de neige dans le bloc ``|| basic: montrer LEDs ||``


```blocks

basic.showLeds(`
    . # # # .
    # . . . #
    # . . . #
    # . . . #
    . # # # .
    `)


```

## Étape 3

Crée trois nouvelles fonctions à l'aide du bloc ``||functions: Crée une fonction||``.

Nomme les fonctions : neige1, neige2 et neige3.

```blocks

function neige1 () {
	
}
function neige2 () {
	
}
function neige3 () {
	
}

```

## Étape 4

Ajoute le bloc ``||functions: appel neige1||`` dans le bloc ``||input: lorsque secouer||``.

Ajoute le bloc ``||functions: appel neige2||`` sous le bloc ``||functions: appel neige1||``.

Ajoute le bloc ``||functions: appel neige1||`` sous le bloc ``||functions: appel neige2||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    neige1()
    neige2()
    neige3()
})
function neige1 () {
	
}
function neige2 () {
	
}
function neige3 () {
	
}

```

## Étape 5

Ajoute le bloc ``||led: allumer x / y||`` dans le bloc ``||functions: fonction neige1||``.

```blocks

function neige1 () {
    led.plot(0, 0)

```

## @showdialog

Voici les coordonnées x,y des LEDs sur l'écran du micro:bit.

Le but est d'allumer et/ou d'éteindre uniquement les LEDs aux coordonnées 1 à 3 pour x et y. 

Autrement dit, uniquement les LEDs à l'intérieur de la boule de neige.

![Atelier](https://pxt.azureedge.net/blob/dcab173218997aba45eb174b25cb128e3172bbb1/static/courses/csintro/coordinates/microbit-led-coords.png)


## Étape 6

Ajoute le bloc ``||math: choisir au hasard||`` à la valeur "x" et "y" du bloc ``||led: allumer x / y||``.

Modifie les valeurs de x (1 et 3) et y (1 et 3).

```blocks

function neige1 () {
    led.plot(randint(1, 3), randint(1, 3))
}

```

## Étape 7

Ajoute le bloc ``||basic: pause (ms) 100||`` sous le bloc ``||led: allumer x / y||``.

```blocks

function neige1 () {
    led.plot(randint(1, 3), randint(1, 3))
    basic.pause(100)
}

```

## Étape 8

Ajoute le bloc ``||led: éteindre x / y||`` sous le bloc ``||basic: pause (ms) 100||``.

Ajoute le bloc ``||math: choisir au hasard||`` dans la valeur "x" et "y" du bloc ``||led: éteindre x / y||``.

Modifie les valeurs de x (1 et 3) et y (1 et 3).

```blocks

function neige1 () {
    led.plot(randint(1, 3), randint(1, 3))
    basic.pause(100)
    led.unplot(randint(1, 3), randint(1, 3))
}

```

## Étape 9

Répète les mêmes étapes pour le bloc ``||functions: fonction neige2||`` et le bloc ``||functions: fonction neige3||``.

## Étape 10

Télécharge le programme dans le micro:bit.

Teste le programme!

Que remarques-tu ?