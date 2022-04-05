# Niveau 1

# Tutoriel 1

## @showdialog

Fais apparaître ton prénom lorsque le micro:bit est activé.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||basic: toujours||``.


```blocks

basic.forever(function () {
    basic.showString("Hello!")
})

```

## Étape 3

Efface le mot "Hello" du bloc ``|| basic: afficher texte ||``.

Écris ton prénom dans le ``|| basic: afficher texte ||`` (ex. : Seb).

```blocks

basic.forever(function () {
    basic.showString("Hello!")
})

```
## Étape 4

Télécharge le programme dans le micro:bit.

Teste le programme!