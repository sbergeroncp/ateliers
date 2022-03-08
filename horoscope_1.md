# Horoscope

## @showdialog

Fais apparaître des éléments aléatoires sur l'écran du micro:bit.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Mois||``. 

Ajoute le bloc ``||variables: définir Mois à "0"||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Mois = 0

```

## Étape 3


Remplace la valeur "0" du bloc  ``||variables: définir Mois à "0"||`` par le bloc ``||arrays: tableau vide +||``.


```blocks

let Mois: number[] = []

```

## Étape 4


Remplace la case vide du bloc ``||arrays: tableau vide +||`` par le bloc ``||text: Janvier||``.

```blocks

let Mois = ["Janvier"]

```

## Étape 5


Ajoute les cases pour les autres mois de l'année à l'aide des blocs ``||text: texte||``

N'écris pas les accents (ex. : Février = Fevrier).

```blocks

let Mois = [
"Janvier",
"Fevrier",
"Mars",
"Avril",
"Mai",
"Juin",
"Juillet",
"Aout",
"Septembre",
"Octobre",
"Novembre",
"Decembre"
]

```

## Étape 6

Conserve ta séquence de programmation et ajoute celle-ci.

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.


```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("Hello!")
})

```

# Étape 7

Remplace le mot "Hello" du bloc ``|| basic: afficher texte ||`` par le bloc ``||arrays: obtenir une valeur aléatoire||``.


```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("" + (Mois._pickRandom()))
})

```