# Niveau 5

# Un circuit électrique et numérique

## @showdialog 

Programme un éclairage de sécurité.
 
![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_f_1.jpg?raw=true) 

## Étape 1 

Supprime le bloc ``|| basic:au démarrage ||``. 

## Étape 2 

 Ajoute le bloc ``|| logic: "si alors sinon"  ||`` dans le bloc ``|| basic:toujours ||``. 
 

```blocks 

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

``` 


## Étape 3 
 
Ajoute le bloc ``|| input: niveau d'intensité lumineuse  ||`` dans le bloc ``|| logic:"0 < 0"||``. 
 
Modifie la valeur de droite ``|| logic:"0 < 0"||`` à 40.

Autrement dit, "si l'intensité de lumière est inférieure à "40"... un événement doit se produire.
 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
    	
    } else {
    	
    }
})

``` 

## Étape 4 
 
Ajoute le bloc ``|| pins: écrire sur la broche  ||`` sous la condition ``|| logic: "si alors sinon"  ||``. 
 
Modifie les valeurs du bloc ``|| pins: écrire sur la broche  ||``.

Écrire sur la broche "P0" la valeur "1". La valeur "1" permet au courant de passer dans le circuit.

 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
    	
    }
})

``` 

## Étape 6 
 
Ajoute le bloc ``|| pins: écrire sur la broche  ||`` sous la condition ``|| logic: "si alors sinon"  ||``. 
 
Modifie les valeurs du bloc ``|| pins: écrire sur la broche  ||``.

Écrire sur la broche "P0" la valeur "0". La valeur "0" empêche le courant de passer dans le circuit.

 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 7 
 
Crée une ``|| variables: LED  ||`` et donne lui le nom ``|| variables: LED  ||``. 

Ajoute le bloc ``|| variables: définir LED à "0" ||`` sous le bloc ``|| basic: toujours  ||``. 

```blocks

let LED = 0
basic.forever(function () {
    LED = 0
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

```

## Étape 8
 
Ajoute le bloc ``|| input: niveau de luminosité  ||`` dans le bloc ``|| variables: définir "LED" à "0"  ||``.

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 

## Étape 9
 
Ajoute le bloc ``|| variables: LED  ||`` dans le bloc ``|| basic: afficher nombre  ||`` sous la condition "si".

```blocks 

let LED = 0
basic.forever(function () {
    LED = input.lightLevel()
    if (input.lightLevel() < 40) {
        basic.showNumber(Luminosité)
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
    }
})

``` 


## @showdialog 

Félicitations! Tu as terminé de programmer un éclairage de sécurité.

Pour tester la séquence de programmation, télécharge le programme dans le micro:bit.

