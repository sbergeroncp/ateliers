## @showdialog

Le test ultime de l'amitié !

![Atelier](https://i.pinimg.com/originals/e9/ff/44/e9ff4450d23b0f05a45840d9d75d7c10.png)

## Étape 1

Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer nombre ||`` dans le bloc ``|| input: lorsque la broche P0 est activée ||``.


```blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showNumber(0)
})

```

## Étape 3

Remplace la valeur "0" par le bloc ``|| math: choisir au hasard de 0 à 10||``.

Modifie la valeur de "10" par "100"  .

```blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showNumber(randint(0, 100))
})

```

## Étape 4

Ajoute le bloc ``|| basic: pause (ms) 2000 ||`` sous le bloc ``|| basic: montrer nombre ||``.


```blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showNumber(randint(1, 100))
    basic.pause(2000)
    })

```

## Étape 5

Ajoute le bloc ``|| basic: effacer l'écran ||`` sous le bloc ``|| basic: pause (ms) 2000 ||``.

```blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showNumber(randint(1, 100))
    basic.pause(2000)
    basic.clearScreen()
})

```

## Étape 6

Télécharge le programme dans le micro:bit.

Teste le programme avec les membres de ton équipe!

![Atelier](https://i.pinimg.com/originals/e9/ff/44/e9ff4450d23b0f05a45840d9d75d7c10.png)

Tiens la main d'un élève dans le but de créer un circuit électrique.

Ensuite, un élève appuie sur la broche "P0" pendant qu'un autre élève appuie sur la broche "GND".

Plus le nombre est élevé, plus votre amitié est solide! C'est scientifique.