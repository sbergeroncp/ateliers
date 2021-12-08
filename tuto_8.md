## @showdialog

Pile ou face ?

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``||logic: "si alors sinon"||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 3

Remplace la valeur "vrai" dans le bloc ``||logic: "si alors sinon"||`` par le bloc ``||math: choisir au hasard vrai ou faux||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
    	
    } else {
    	
    }
})

```

## Étape 4

Ajoute le bloc ``||basic: montrer l'icone||`` dans le bloc ``||logic: si||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Ghost)
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||basic: montrer l'icone||`` dans le bloc ``||logic: alors||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Ghost)
    } else {
        basic.showIcon(IconNames.Square)
    }
})

```

## Étape 6

Ajoute le bloc ``||loops: répéter 2 fois||`` au-dessus du bloc ``||logic: "si alors sinon"||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
    	
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Ghost)
    } else {
        basic.showIcon(IconNames.Square)
    }
})

```

## Étape 7



Ajoute les blocs ``||basic: montrer l'icone||`` dans le bloc ``||loops: "répéter deux fois"||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 2; index++) {
        basic.showIcon(IconNames.Diamond)
        basic.showIcon(IconNames.SmallDiamond)
    }
    if (Math.randomBoolean()) {
        basic.showIcon(IconNames.Ghost)
    } else {
        basic.showIcon(IconNames.Square)
    }
})

```

## Étape 8

Télécharge le programme dans le micro:bit.

Teste le programme!

Manipule le micro:bit. Que remarques-tu?
