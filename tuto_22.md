# Niveau 5

# Un circuit électrique et numérique! 

## @showdialog  

Programme un éclairage de sécurité.
 
![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_f_1.jpg?raw=true) 

## Étape 1 

Supprime le bloc ``|| basic:au démarrage ||``. 

## Étape 2 

Ajoute le bloc ``|| logic: "si vrai alors sinon"  ||`` dans le bloc ``|| basic:toujours ||``. 
 

```blocks 

basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})

``` 

## Étape 3 

Remplace la valeur ``|| logic:"vrai"||`` par le bloc ``|| logic:"0 < 0"||`` dans le bloc ``|| logic: "si vrai alors sinon"||``. 
 
Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (0 < 0) {
    	
    } else {
    	
    }
})
```

## Étape 4 
 
Modifie la valeur "0" (gauche) du bloc ``|| logic:"0 < 0"||`` par le bloc ``|| input: niveau d'intensité lumineuse  ||``. 
 
Modifie la valeur "0" (droite) du bloc ``|| logic:"0 < 0"||`` par la valeur "40".

Autrement dit, "si l'intensité de lumière est inférieure à "40"... un événement doit se produire.

```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
    	
    } else {
    	
    }
})

``` 

## Étape 5 
 
Ajoute le bloc ``|| pins: écrire sur la broche  ||`` sous la condition ``|| logic: "si alors"  ||``. 
 
La valeur "1" permet au courant de passer dans le circuit.

Regarde l'indice pour connaître les valeurs à changer.
 
```blocks 

basic.forever(function () {
    if (input.lightLevel() < 40) {
        pins.digitalWritePin(DigitalPin.P0, 1)
    } else {
    	
    }
})

``` 

## Étape 6 
 
Ajoute le bloc ``|| pins: écrire sur la broche  ||`` sous la condition ``|| logic: "sinon"  ||``. 

La valeur "0" empêche le courant de passer dans le circuit.

Regarde l'indice pour connaître les valeurs à changer.

 
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
 
Crée une ``|| variables: variable  ||`` et donne lui le nom ``|| variables: LED  ||``. 

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
 
Remplace la valeur "0" du bloc ``|| variables: définir "LED" à "0"  ||`` par le bloc ``|| input: niveau d'intensité luminosité  ||``.

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
 
Ajoute le bloc ``|| variables: LED  ||`` dans le bloc ``|| basic: afficher nombre  ||`` sous la condition ``|| logic: "si"  ||``.

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

