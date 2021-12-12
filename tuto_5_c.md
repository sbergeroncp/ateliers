## @showdialog

Distanciation sociale entre élèves!

## Étape 1

Ajoute le bloc ``||radio: radio définir groupe "1"||`` dans le bloc ``||basic: au démarrage||``.

```blocks

radio.setGroup(1)
})

```

## Étape 2

Ajoute le bloc ``||radio: envoyer le nombre "0" par radio||`` dans le bloc ``||basic: toujours||``.

```blocks

basic.forever(function () {
    radio.sendNumber(0)
})

```

## Étape 3

Ajoute le bloc ``||logic: "si alors sinon"||`` dans le bloc ``||radio: quand une donnée est reçue par radio||``.

```blocks

radio.onReceivedNumber(function (receivedNumber) {
    if (true) {
    	
    } else {
    	
    }
})


```

## Étape 4

Remplace la valeur "vrai" par le bloc ``||logic: "0 < 0)"||`` dans le bloc ``||logic:"si alors sinon" ||``.

```blocks

radio.onReceivedString(function (receivedNumber) {
    if (0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 5

Remplace la valeur "0" (gauche) par le le bloc ``||radio: paquet reçu force du signal||``.

Remplace la valeur "0" (droite) par la valeur -65.

```blocks

radio.onReceivedString(function (receivedNumber) {
    if (radio.receivedPacket(RadioPacketProperty.SignalStrength) < -65) {
    	
    } else {
    	
    }
})

```

## Étape 6

Ajoute le bloc ``||basic: montre l'icône||`` sous le bloc ``||logic: si||``.

Ajoute le bloc ``||basic: montre l'icône||`` sous le bloc ``||logic: sinon||``.

```blocks

radio.onReceivedString(function (receivedNumber) {
    if (radio.receivedPacket(RadioPacketProperty.SignalStrength) < -65) {
        basic.showIcon(IconNames.No)
    } else {
        basic.showIcon(IconNames.Yes)
    }
})


```

## Étape 7

Télécharge le programme dans le micro:bit.

Teste le code avec un autre élève qui a le même programme.

À quelle distance le micro:bit te permet-il de t'approcher d'un autre élève ?