## @showdialog

Fais apparaître une image lorsque le micro:bit est activé.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer l'icône ||`` dans le bloc ``||basic: toujours||``.

Choisis une icône dans le bloc ``|| basic: montrer l'icône ||``.


```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})

```

## Étape 3

Télécharge le programme dans le micro:bit.

Teste le programme!