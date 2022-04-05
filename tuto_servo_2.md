# Tutoriel - Arrosage automatisé et servomoteur

## @showdialog

Programme le servomoteur.

## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.

Modifie la valeur de la ``||pins: broche ||`` ``||pins: P0 ||`` pour ``||pins: P1 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 0 ||``.

```blocks
input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 0)
})

```

## @showdialog

Assure-toi que la paille pointe vers la terre lorsque l'angle est à 0.

## @showdialog

Maintenant, tu dois déterminer l'angle qui permet au servomoteur de faire basculer la paille dans l'eau.

## @showdialog

Parfois, il vaut mieux faire réaliser des sauts (ex. : 25 degrés, 30.., 35.., 45.., etc) au servomoteur pour obtenuir un angle égal ou supérieur à 90.

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

Modifie la valeur du bloc ``||basic: pause (ms) 100 ||`` pour ``||basic: 200 ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(200)
    })
```

## Étape 5

Ajoute le bloc ``||pins: régler position servo ||`` sous le bloc ``||basic: pause (ms) 200 ||``.

Modifie le ``||pins: degré ||`` pour ``||pins: 90 ||``.

```blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(200)
    pins.servoWritePin(AnalogPin.P1, 90)
    })
```
## Étape 6

Ajoute le bloc ``||basic: pause (ms) 100 ||`` sous le bloc ``||pins: régler position servo ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.

Modifie la valeur du bloc ``||basic: pause (ms) 100 ||`` pour ``||basic: 200 ||``.

```blocks

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
    basic.pause(200)
    pins.servoWritePin(AnalogPin.P1, 90)
    basic.pause(200)
})

```
## @showdialog

Assure-toi que la paille pointe vers la terre lorsque l'angle est à 0.

Assure-toi également que la paille soit dans l'eau lorsque l'angle est supérieur à 90.

Télécharge la programmation du servomoteur dans le micro:bit.

Bonne expérimentation!