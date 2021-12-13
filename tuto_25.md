# Niveau 5

# Un circuit électrique clignotant !

## @showdialog 

Transforme ton micro:bit en une alarme avec une lumière LED. 

## Étape 1 

Supprime le bloc  ``|| basic:au démarrage ||``. 

## Étape 2 

Ajoute le bloc ``|| logic: "si alors sinon" ||`` sous le bloc ``||basic:toujours||``.

Ajoute le bloc ``|| logic: ou ||`` dans le bloc ``|| logic: "si alors sinon" ||``. 

Ajoute les blocs ``|| logic: 0 > 0 ||`` et ``|| logic: 0 < 0 ||`` dans le bloc ``|| logic: ou ||``
 

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (0 > 0 || 0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 3 

Remplace la valeur 0 du bloc ``|| logic: 0 > 0 ||`` (gauche) par le bloc ``|| input: accéléromètre (mg) x||``.

Remplace la valeur 0 du bloc ``|| logic: 0 > 0 ||`` (droite) par le bloc ``|| input: accéléromètre (mg) x||``.

Remplace les valeurs "0" par "50".

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 50 || input.acceleration(Dimension.X) < 50) {
    	
    } else {
    	
    }
})

```

## Étape 4 

Ajoute le bloc ``|| basic: montrer l'icone ||`` sous le bloc ``|| logic: "si alors" ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Ajoute le bloc ``|| basic: montrer l'icone ||`` sous le bloc ``|| basic: pause (ms) 200 ||``.

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``||basic:montrer l'icône||``.

Ajoute le bloc ``|| basic: pause (ms) 200 ||`` sous le bloc ``|| pins: écrire sur la broche ||``.

Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 50 || input.acceleration(Dimension.X) < 50) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        basic.showIcon(IconNames.SmallSquare)
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.pause(200)
    } else {
    	
    }
})

```

## Étape 5 

Ajoute le bloc ``|| pins: écrire sur la broche ||`` sous le bloc ``|| logic: "sinon" ||``.

Ajoute le bloc ``|| basic: effacer l'écran ||`` sous le bloc ``|| pins: écrire sur la broche ||``.


Regarde l'indice pour connaître les valeurs à changer.

```blocks 

basic.forever(function () {
    if (input.acceleration(Dimension.X) > 50 || input.acceleration(Dimension.X) < 50) {
        basic.showIcon(IconNames.Square)
        pins.digitalWritePin(DigitalPin.P0, 1)
        basic.pause(200)
        basic.showIcon(IconNames.SmallSquare)
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.pause(200)
    } else {
        pins.digitalWritePin(DigitalPin.P0, 0)
        basic.clearScreen()
    }
})

```

## @showdialog 

Félicitations! Tu as terminé la programmation de ton  circuit électrique.

Branche maintenant ton circuit.

Vérifie que la lumière LED clignote lorsque le micro:bit est déplacé.