## Étape A
Crée une séquence de programmation de ton choix à l'aide des blocs.

Tu dois utiliser au moins une fois tous les blocs.

```blocks
input.onButtonPressed(Button.A, function () {
    basic.showString("Hello!")
})
input.onGesture(Gesture.Shake, function () {
    for (let index = 0; index < 4; index++) {
        basic.showIcon(IconNames.Heart)
        basic.pause(100)
    }
})
basic.forever(function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . # . .
        . . . . .
        . . . . .
        `)
})
```