## @showdialog

Une boussole pour s'orienter!

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne lui le nom ``||variables:Degres||``. (sans accent sur le "é")

Ajoute le bloc ``||variables: définir Degres à "0"||`` dans le bloc ``||basic: toujours||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = 0
})

```

## Étape 3

Remplace la valeur "0" dans le bloc ``||variables: définir Main||`` par le bloc ``||input: direction de la boussole||``.


```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
})

```

## Étape 4

Ajoute le bloc ``||logic: si vrai alors sinon si||`` sous le bloc ``||variables: définir Degres||``.

Ajoute 4 conditions en tout.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (true) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 5

Ajoute le bloc ``||logic: "0" = "0"||`` dans le bloc ``||logic: si||``.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (0 < 0) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 6

Remplace la valeur "0" de gauche du bloc ``||logic: "0" = "0"||`` par le bloc ``||variables:Degres||``.

Remplace la valeur "0" de droite du bloc ``||logic: "0" = "0"||`` par la valeur "45".

La valeur 45 représente la coordonnée nord-est.

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
    	
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``||basic: afficher le texte||`` sous le bloc ``||logic: "si Degres < 45"||``.

Remplace la valeur "Hello" de droite du bloc ``||basic: afficher le texte||`` par la lettre "N".

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
        basic.showString("N")
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})

```

## Étape 8

Ajoute le bloc ``||basic: afficher le texte||`` sous le bloc ``||logic: sinon||``.

Remplace la valeur "Hello" de droite du bloc ``||basic: afficher le texte||`` par la lettre "N".

```blocks

let Degres = 0
basic.forever(function () {
    Degres = input.compassHeading()
    if (Degres < 45) {
        basic.showString("N")
    } else if (false) {
    	
    } else if (false) {
    	
    } else {
        basic.showString("N")
    }
})

```

## @showdialog

Oups! Les étapes pour programmer les autres points cardinaux ont disparu.

Programme le micro:bit pour qu'il puisse afficher les autres points cardinaux.

La valeur < 45 représente le point cardninal ``||input: nord||``. La valeur < 135 représente le point cardninal ``||input: est||``.

La valeur < 225 représente le point cardninal ``||input: sud||``. La valeur < 315 représente le point cardninal ``||input: ouest||`` .

## Étape 8

Télécharge le programme dans le micro:bit.

Teste le programme ! 

Quel élément retrouve-t-on au nord ? au sud ? à l'est ? à l'ouest ?