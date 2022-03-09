# horos

## @showdialog

Fais apparaître des éléments aléatoires sur l'écran du micro:bit.

## Étape 1

Supprime le bloc ``||basic:toujours||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Mois||``. 

Ajoute le bloc ``||variables: définir Mois à||`` ``||arrays: tableau de a b c||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Mois = ["a", "b", "c"]

```

## Étape 3

Remplace les cases du bloc ``||arrays: tableau de a b c||`` par le nom des douze mois.

```blocks

let Mois = ["Janvier", "Février", "Mars"]

```

## Étape 4

Conserve la séquence de programmation et ajoute celle-ci.

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||input: lorsque le bouton A est pressé||``.


```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("Hello!")
})

```

## Étape 5

Remplace le mot ``|| basic: Hello ||`` du bloc ``|| basic: afficher texte ||`` par le bloc ``||arrays: obtenir une valeur aléatoire depuis||`` ``||variables: Mois||``.


```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("" + (Mois._pickRandom()))
})
let Mois: string[] = []
Mois = ["Janvier", "Février", "Mars"]

```

## Étape 6

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Qualités||``. 

Ajoute le bloc ``||variables: définir Qualités à||`` ``||arrays: de tableau a b c||`` dans le bloc ``||basic: au démarrage||``.

```blocks

let Qualités = ["a", "b", "c"]

```

## Étape 7

Remplace las cases du bloc ``||arrays: tableau de a b c||`` par le nom des douze qualités.

Regarde l'indice.

```blocks

let Qualités = ["Aimable", "Calme", "Compétent", "Curieux", "Original", "Sérieux", "Réfléchi", "Responsable", "Optimiste", "Créatif", "Innovateur", "Sociable"]

```

## Étape 8

Conserve la séquence de programmation et ajoute celle-ci.

Ajoute le bloc ``|| basic: afficher texte ||`` dans le bloc ``||input: lorsque le bouton B est pressé||``.


```blocks

input.onButtonPressed(Button.B, function () {
    basic.showString("Hello!")
})

```

## Étape 9

Remplace le mot ``|| basic: Hello ||`` du bloc ``|| basic: afficher texte ||`` par le bloc ``||arrays: obtenir une valeur aléatoire depuis||`` ``||variables: Qualités||``.


```blocks

input.onButtonPressed(Button.B, function () {
    basic.showString("" + (Qualites._pickRandom()))
})
let Qualites: string[] = []
Qualités = ["Aimable", "Calme", "Compétent", "Curieux", "Original", "Sérieux", "Réfléchi", "Responsable", "Optimiste", "Créatif", "Innovateur", "Sociable"]

```

## Étape 10

Conserve les séquences de programmation et ajoute celle-ci.

Ajoute le bloc ``|| basic: montrer le nombre ||`` dans le bloc ``||input: lorsque secouer||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showNumber(0)
})

```

## Étape 11

Remplace la valeur ``|| basic: 0 ||`` du bloc ``|| basic: montrer le nombre ||`` par le bloc ``|| math: choisir au hasard de 0 à 10 ||``.

Remplace la valeur ``|| math: 10 ||`` du bloc ``|| math: choisir au hasard de 0 à 10 ||`` par ``|| math: 100 ||``.

```blocks

input.onGesture(Gesture.Shake, function () {
    basic.showNumber(randint(0, 10))
})

```
