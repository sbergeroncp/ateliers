# Tutoriel - Arrosage automatisé - Servomoteur


## @showdialog

Programme le servomoteur.

## Étape 1

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 45 ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 45)
})

```

## Étape 2

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 90 ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 90)
})

```

## Étape 3

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A+B est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 0 ||``.

```blocks
input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 0)
})

```

## Étape 4

Télécharge la programmation du servomoteur dans le micro:bit.

Bonne expérimentation!