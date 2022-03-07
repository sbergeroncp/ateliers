# Tutoriel 1

## @showdialog

Fais apparaître tes initiales lorsque le micro:bit est activé.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||basic: toujours||``.

Efface le mot "Hello" du bloc ``|| basic: afficher texte ||``.

Écris tes initiales (ex. : Sébastien Bergeron = SB) dans bloc ``|| basic: afficher texte ||``.

```blocks

basic.forever(function () {
    basic.showString("Hello!")
})

```

## Étape 3

Télécharge le programme dans le micro:bit.

Teste le programme!