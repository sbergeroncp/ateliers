# Niveau 5

# Un circuit électrique avec un servomoteur! 

## @showdialog 

Transforme ton micro:bit en un circuit électrique avec un servomoteur! 
 
![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_7.jpg?raw=true) 

## Étape 1 

Supprime les blocs ``|| basic:au démarrage ||`` et ``|| basic:toujours ||``. 

## Étape 2 

 Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton A est pressé||``. 
 
Modifie la valeur du bloc ``|| pins: régler position servo  ||``.

Écris à "45" degrés.
 

```blocks 

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P0, 45)
})

``` 

## Étape 3 
 
Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton B est pressé||``. 
 
Modifie la valeur du bloc ``|| pins: régler position servo  ||``.

Écris à "90" degrés.
 

```blocks 

input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P0, 90)
})

``` 

## Étape 4 
 
Ajoute le bloc ``|| pins: régler position servo  ||`` dans le bloc ``||input:lorsque le bouton A+B est pressé||``. 
 
Modifie le valeur du bloc ``|| pins: régler position servo  ||``.

Écris à "0" degrés.
 

```blocks 

input.onButtonPressed(Button.AB, function () {
    pins.servoWritePin(AnalogPin.P0, 0)
})

``` 


## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_1.jpg?raw=true) 

Branche une pince alligator dans le port "P0" du micro:bit.

## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_2.jpg?raw=true) 

Branche une pince alligator dans le port "3V" du micro:bit.

## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_3.jpg?raw=true) 

Branche une pince alligator dans le port "GND" du micro:bit.


## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_4.jpg?raw=true) 

Relis la pince alligator branchée dans le port "P0" du micro:bit dans la branche jaune du servomoteur.


## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_5.jpg?raw=true) 

Relis la pince alligator branchée dans le port "3V" du micro:bit dans la branche centrale du servomoteur.

## @showdialog 

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_6.jpg?raw=true) 

Relis la pince alligator branchée dans le port "GND" du micro:bit dans la dernière branche du servomoteur.

## @showdialog 

Félicitations! Tu as terminé les branchements et la programmation de ton  circuit électrique et numérique.

![CSSBF](https://github.com/sbergeroncp/mon-makecode/blob/master/atelier_b_7.jpg?raw=true) 

Teste maintenant ton circuit!