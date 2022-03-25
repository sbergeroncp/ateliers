# Tutoriel - Arrosage automatisé - Capteur d'humidité et servomoteur

## @showdialog

Programme le capteur d'humidité et le servomoteur.


## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``|| loops: every 500 ms ||``.

Remplace la valeur par ``|| loops: 500 ms ||`` par ``|| loops: 10000 ms ||``.

Si 1 seconde = ``|| loops: 1000 ms ||``, alors 10 secondes = ``|| loops: 10000 ms ||``.

```blocks
loops.everyInterval(10000, function () {
	
})

```

## Étape 3

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Terre||``.

Ajoute le bloc ``||variables: définir Terre à "0"||`` dans le bloc ``|| loops: every 10000 ms ||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = 0
})

```

## Étape 4

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Terre ||`` par le bloc ``||pins: lire la broche analogique P0||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
})

```

## Étape 5

Ajoute les blocs ``||basic: montrer nombre||`` et ``||basic: pause (ms) 100 ||`` sous le bloc ``||variables: définir Terre ||``.

Remplace la valeur ``||basic: 100||`` du bloc ``||basic: pause (ms) ||`` par ``||basic: 1000 ||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(0)
    basic.pause(1000)
})

```

## Étape 6

Remplace la valeur ``||basic: 0||`` du bloc ``||basic: montrer nombre||`` par le bloc ``||math: arrondi||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(0))
    basic.pause(1000)
})

```

## Étape 7

Remplace la valeur ``||math: 0||`` du bloc ``||math: arrondi||`` par le bloc ``||variables: Terre||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
})

```

## Étape 8

Ajoute le bloc ``||logic: si vrai alors sinon ||`` sous le bloc ``||basic: pause (ms) 1000 ||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (true) {
    	
    } else {
    	
    }
})
```

## Étape 9

Remplace la valeur  ``|| vrai ||`` par le bloc ``||logic: 0 > 0  ||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (0 > 0) {
    	
    } else {
    	
    }
})
```

## Étape 10

Remplace la valeur  ``||logic: 0  ||`` de gauche du bloc ``||logic: 0 > 0  ||`` par le bloc ``||variables: Terre||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
    	
    } else {
    	
    }
})
```

## Étape 11

Remplace la valeur  ``||logic: 0  ||`` de droite du bloc ``||logic: 0 > 0  ||`` par la valeur calculée.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
    	
    } else {
    	
    }
})
```

## Étape 12

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||logic: si alors  ||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: l'angle souhaité ||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
        pins.servoWritePin(AnalogPin.P1, 110)
    } else {
    	
    }
})
```

## Étape 13

Ajoute le bloc ``||basic: pause (ms) 100 ||`` sous le bloc ``||pins: régler position servo ||``.

Modifie la valeur ``||basic: 100 ||`` du bloc ``||basic: pause (ms) ||`` par ``||basic: 2000 ||``

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
        pins.servoWritePin(AnalogPin.P1, 110)
        basic.pause(2000)
    } else {
    	
    }
})
```

## Étape 14

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||basic: pause (ms) 2000  ||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: l'angle souhaité ||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
        pins.servoWritePin(AnalogPin.P1, 110)
        basic.pause(2000)
        pins.servoWritePin(AnalogPin.P1, 0)
    } else {
    	
    }
})
```

## Étape 15

Ajoute le bloc ``||basic: montrer l'icône ||`` sous le bloc ``||logic: sinon  ||``.

```blocks
let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.analogReadPin(AnalogPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
    if (Terre > 0) {
        pins.servoWritePin(AnalogPin.P1, 110)
    } else {
        basic.showIcon(IconNames.Heart)
    }
})
```

## Étape 16

Ajoute le bloc ``||basic: montrer nombre ||`` et le bloc ``||basic: pause (ms) 1000 ||`` dans le bloc ``||input: lorsque le bouton A est pressé  ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(0)
    basic.pause(1000)
})
```

## Étape 17

Remplace la valeur ``||basic: 0||`` du bloc ``||basic: montrer nombre||`` par le bloc ``||math: arrondi||``.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showNumber(Math.round(0))
    basic.pause(1000)
})
```

## Étape 18

Remplace la valeur ``||math: 0||`` du bloc ``||math: arrondi||`` par le bloc ``||variables: Terre||``.

```blocks
input.onButtonPressed(Button.A, function () {
    let Terre = 0
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
})
```

## Étape 19

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||input: lorsque le bouton B est pressé  ||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: l'angle souhaité ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P1, 110)
})
```

## Étape 20

Ajoute le bloc ``||basic: pause (ms) 100 ||`` sous le bloc ``||pins: régler position servo ||``.

Modifie la valeur ``||basic: 100 ||`` du bloc ``||basic: pause (ms) ||`` par ``||basic: 2000 ||``

```blocks
input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P1, 0)
    basic.pause(2000)
})
```

## Étape 21

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||basic: pause (ms) 2000  ||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: l'angle souhaité ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.digitalWritePin(DigitalPin.P1, 110)
    basic.pause(2000)
    pins.digitalWritePin(DigitalPin.P1, 0)
})
```

## Étape 22

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc``||basic: au démarrage ||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: l'angle souhaité ||``.

Assure-toi que la paille ne touche ni à l'eau ni à la terre au démarrage.

```blocks
pins.servoWritePin(AnalogPin.P1, 45)
```