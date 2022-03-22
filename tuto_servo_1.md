Système d'arrosage automatisé

## Étape 1

Supprime les blocs ``|| basic:au démarrage ||`` et ``|| basic:toujours ||``. 

## Étape 2 

 Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``. 
 
Modifie la broche de ``|| pins: régler position servo  ||`` pour ``|| pins: P1  ||``.

Modifie la valeur du ``|| pins: degré ||`` pour ``|| pins: 45 ||``.
 

```blocks 

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
})

``` 

## Étape 3 
 
Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton B est pressé||``. 
 
Modifie la broche de ``|| pins: régler position servo  ||`` pour ``|| pins: P1  ||``.

Modifie la valeur du ``|| pins: degré ||`` pour ``|| pins: 90 ||``.
 

```blocks 

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
})

``` 

## Étape 4 
 
Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``. 
 
Modifie la broche de ``|| pins: régler position servo  ||`` pour ``|| pins: P1  ||``.

Modifie la valeur du ``|| pins: degré ||`` pour ``|| pins: 0 ||``.
 

```blocks 

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
})

``` 

## Étape 5 

Télécharge la programmation dans le micro:bit.

Teste maintenant le circuit.

```blocks 

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 45)
})

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
})

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
})

``` 