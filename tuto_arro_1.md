# Tutoriel - Arrosage automatisé - Capteur d'humidité

## @showdialog
Dans ce tutoriel, je te présente comment programmer le capteur d'humidité.

## Étape 1

Supprime les blocs ``||basic: au démarrage||`` et ``||basic: toujours||``.

## Étape 2

Ajoute le bloc ``|| loops: every 500 ms ||``.

Remplace la valeur par ``|| loops: 500 ms ||`` par ``|| loops: 10000 ms ||``.

Nous souhaitons que le micro:bit prenne des valeurs à toutes les 10 secondes. 

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
    Terre = pins.digitalReadPin(DigitalPin.P0)
})

```

## Étape 5

Ajoute les blocs ``||basic: montrer nombre||`` et ``||basic: pause (ms) 100 ||`` sous le bloc ``||variables: définir Terre ||``.

Remplace la valeur ``||basic: 100||`` du bloc ``||basic: pause (ms) ||`` par ``||basic: 1000 ||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.digitalReadPin(DigitalPin.P0)
    basic.showNumber(0)
    basic.pause(1000)
})

```

## Étape 6

Remplace la valeur ``||basic: 0||`` du bloc ``||basic: montrer nombre||`` par le bloc ``||math: arrondi||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.digitalReadPin(DigitalPin.P0)
    basic.showNumber(Math.round(0))
    basic.pause(1000)
})

```

## Étape 7

Remplace la valeur ``||math: 0||`` du bloc ``||math: arrondi||`` par le bloc ``||variables: Terre||``.

```blocks

let Terre = 0
loops.everyInterval(10000, function () {
    Terre = pins.digitalReadPin(DigitalPin.P0)
    basic.showNumber(Math.round(Terre))
    basic.pause(1000)
})

```

## Étape 8

Télécharge la programmation du capteur d'humidité dans le micro:bit.

Bonne expérimentation!