# Niveau 5

# Un circuit électrique avec un servomoteur et une lumière LED. 

## @showdialog 

Transforme ton micro:bit en un circuit électrique avec un servomoteur! 

## Étape 1 

Supprime le bloc  ``|| basic:toujours ||``. 

## Étape 2 

 Ajoute le bloc ``|| pins: régler position servo broche ||`` dans le bloc ``||basic:au démarrage||``.

 Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| pins: régler position servo broche ||``. 
 
 Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| pins: écrire sur la broche ||``. 

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

pins.servoWritePin(AnalogPin.P0, 0)
pins.digitalWritePin(DigitalPin.P1, 0)
basic.showIcon(IconNames.No)

```
## Étape 3 

 Ajoute le bloc ``|| pins: régler position servo broche ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Ajoute le bloc ``|| basic: pause (ms) 500 ||`` sous le bloc ``|| pins: régler position servo broche ||``.

 Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) 500 ||``. 
 
  Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| pins: écrire sur la broche ||``. 

Regarde l'indice pour connaître les valeurs à changer.
 

```blocks 

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 90)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P1, 1)
    basic.showIcon(IconNames.Yes)
})

``` 

## Étape 4 
 
Ajoute le bloc ``|| pins: régler position servo broche ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.

Ajoute le bloc ``|| basic: pause (ms) 500 ||`` sous le bloc ``|| pins: régler position servo broche ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| basic: pause (ms) 500 ||``. 
 
Ajoute le bloc ``|| basic: montrer l'icône  ||`` sous le bloc ``|| pins: écrire sur la broche ||``.
 
 Regarde l'indice pour connaître les valeurs à changer.

```blocks 

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 0)
    basic.pause(500)
    pins.digitalWritePin(DigitalPin.P1, 0)
    basic.showIcon(IconNames.No)
})

``` 

## @showdialog 

Félicitations! Tu as terminé la programmation de ton  circuit électrique avec un servomoteur et une lumière LED.

Branche maintenant ton circuit.

Teste la séquence de programmation.