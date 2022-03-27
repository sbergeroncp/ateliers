# Tutoriel - Arrosage automatisé - Servomoteur


## @showdialog

Programme le servomoteur.


## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 45 ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 45)
})

```

## Étape 3

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 45 ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    })

```

## Étape 4

Ajoute le bloc ``||basic: pause (ms) 100 ||`` sous le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||basic: pause (ms) 100 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 90 ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(200)
    pins.servoWritePin(AnalogPin.P1, 90)
})
```

## Étape 5

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 0 ||``.

```blocks
input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 0)
})

```

## Étape 6

Télécharge la programmation du servomoteur dans le micro:bit.

Bonne expérimentation!