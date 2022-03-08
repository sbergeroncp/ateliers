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


Remplace la valeur ``||variables: 0||``du bloc  ``||variables: définir Mois à "0"||`` par le bloc ``||arrays: tableau vide +||``.


```blocks

let Mois: number[] = []

```

## Étape 4


Remplace la case vide du bloc ``||arrays: tableau vide +||`` par le bloc ``||text: texte||``.

```blocks

let Mois = ["Janvier"]

```

## Étape 5


Ajoute les cases pour les autres mois de l'année à l'aide des blocs ``||text: texte||``.

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

Remplace le mot ``|| basic: Hello ||`` du bloc ``|| basic: afficher texte ||`` par le bloc ``||arrays: obtenir une valeur aléatoire||``.


```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("" + (Mois._pickRandom()))
})

```

## Étape 8

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Qualite||``. 

N'écris pas les accents sur les mots.

Ajoute le bloc ``||variables: définir Qualite à "0"||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Qualite = 0

```

## Étape 9


Remplace la valeur ``||variables: 0 ||`` du bloc ``||variables: définir Qualite à "0"||`` par le bloc ``||arrays: tableau vide +||``.


```blocks

let Qualite: number[] = []

```

## Étape 10


Remplace la case vide du bloc ``||arrays: tableau vide +||`` par le bloc ``||text: texte||``.

```blocks

let Mois = ["texte"]

```

## Étape 11


Ajoute les cases pour 12 qualités en tout à l'aide des blocs ``||text: texte||``.

N'écris pas les accents sur les mots.

```blocks

let Mois = [
"Aimable",
"Calme",
"Competent",
"Curieux",
"Original",
"Serieux",
"Reflechi",
"Responsable",
"Optimiste",
"Creatif",
"Innovateur",
"Sociable"
]

```

## Étape 12

Conserve ta séquence de programmation et ajoute celle-ci.

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.


```blocks

input.onButtonPressed(Button.B, function () {
    basic.showString("Hello!")
})

```

# Étape 13

Remplace le mot ``|| basic: Hello||`` du bloc ``|| basic: afficher texte ||`` par le bloc ``||arrays: obtenir une valeur aléatoire||``.


```blocks

input.onButtonPressed(Button.B, function () {
    basic.showString("" + (Qualite._pickRandom()))
})

```

# Étape 14 

Ajoute le bloc ``|| basic: montrer le nombre ||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showNumber(0)
})

```

# Étape 15 

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer le nombre ||`` par le bloc ``|| math: choisir au hasard de 0 à 10 ||``.

Remplace la valeur ``|| math: 10 ||`` du bloc ``|| math: choisir au hasard de 0 à 10 ||`` par ``|| math: 100 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showNumber(randint(0, 10))
})

```