# 土味情话

```
/*
 * 比闺女更重要的人是谁？当然是娃娘了！ micro:bit 买回来的第一件事就是要对娃娘“表白”呀！
 * 没有比 LED 整列显示字符更简单的方式了，第一个程序，足够简单，足够用于了解 microbit 全流程。
*/

input.onButtonPressed(Button.B, () => {
    game.addScore(1)
})

input.onButtonPressed(Button.A, () => {
    while (true) {
        images.createImage(`
            # . . . #
            # # . # #
            # . # . #
            # . # . #
            # . . . #
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.createImage(`
            . # # # .
            # . . . #
            # . . . #
            # . . . #
            . # # # .
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.createImage(`
            # . . . #
            # # . . #
            # . # . #
            # . . # #
            # . . . #
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.createImage(`
            . # . # .
            . # # . .
            . # . . .
            . # # . .
            . # . # .
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.createImage(`
            # # # # .
            # . . . .
            # # # # .
            # . . . .
            # # # # .
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.createImage(`
            # . . . #
            . # . # .
            . . # . .
            . . # . .
            . . # . .
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(1000)
        images.iconImage(IconNames.Heart).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.iconImage(IconNames.Heart).scrollImage(1, 200)
        control.waitMicros(1000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        images.iconImage(IconNames.Heart).showImage(0, 4000)
        control.waitMicros(4000)
        images.createImage(`
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . .
            `).scrollImage(1, 200)
        control.waitMicros(400)
        game.addScore(1)
    }
})

```
