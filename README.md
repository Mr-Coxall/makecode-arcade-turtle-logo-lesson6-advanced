### @explicitHints true

# Turtle Logo - Lesson #6 - Advanced

## Turtle Logo - Lesson, with variables and sprites #6 @unplugged
**Making the Turtle's do Loops.**

In this lesson you will learn to use loops, to make your code more efficient.
![](https://github.com/Mr-Coxall/makecode-arcade-turtle-logo-lesson6-advanced/raw/main/assets/looping_screenshot.png)

## Step 1
** Follow Along**

Once again, all our programs begin with an ⇢``on start``⇠ block. You will begin with 1 variables called myDuck and then you need to assign a **Turtle Object** using the ⇢``set myTurtle to a Turtle Object with sprite □ of kind Player``⇠ block.
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
```

## Step 2
** Follow Along**

You know from previous lessons how to move forwards and then turn.
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
```

## Step 3
**Try it out**

If I asked you to draw a square, what would you do?

Try out some solutions.

## Step 4
** Follow Along**

Most likely you can up with something like this.
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
```

## Step 5
** Did you know**

When you look at the previous solution, you will notice that the same 2 block were repeated 4 times. In programming this is **a really bad idea**. Repeating yourself encourages errors in your code and is hard to change things if needed.
```blocks
myDuck.moveDirection(TurtleDirection.Forward, 25)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
```

## Step 6
** Did you know**

What we do instead is use a new block, the ⇢``repeat 4 times, do``⇠ block. It is under the "Loops" menu. 
```blocks
for (let index = 0; index < 4; index++) {
}
```

## Step 7
** Follow Along**

Notice that there is a space inside the block. You can place other blocks in there. Since it has the number "4", any code blocks inside it will be executed 4 times. You can always change the 4 to whatever number you would like. 
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
for (let index = 0; index < 4; index++) {
}
```

## Step 8
** Follow Along**

So you can now take your 2 blocks that repeated 4 times and place them inside the ⇢``repeat 4 times, do``⇠ block. This produces a much simpler and easier to maintain program. 
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
for (let index = 0; index < 4; index++) {
    myDuck.moveDirection(TurtleDirection.Forward, 25)
    myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
}
```

## Step 9
** Follow Along**

You could also lift the pen and move your **Turtle Object** over before starting to draw your square. 
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
myDuck.pen(TurtlePenMode.Up)
myDuck.moveDirection(TurtleDirection.Forward, 50)
myDuck.pen(TurtlePenMode.Down)
for (let index = 0; index < 4; index++) {
    myDuck.moveDirection(TurtleDirection.Forward, 25)
    myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
}
```

## Step 9
** Follow Along**

You can also have 2 **Turtle Object** drawing squares. 
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
myDuck.pen(TurtlePenMode.Up)
myDuck.moveDirection(TurtleDirection.Forward, 50)
myDuck.pen(TurtlePenMode.Down)
let myApple = turtle.fromSprite(sprites.create(img`
    . . . . . . . e c 7 . . . . . . 
    . . . . e e e c 7 7 e e . . . . 
    . . c e e e e c 7 e 2 2 e e . . 
    . c e e e e e c 6 e e 2 2 2 e . 
    . c e e e 2 e c c 2 4 5 4 2 e . 
    c e e e 2 2 2 2 2 2 4 5 5 2 2 e 
    c e e 2 2 2 2 2 2 2 2 4 4 2 2 e 
    c e e 2 2 2 2 2 2 2 2 2 2 2 2 e 
    c e e 2 2 2 2 2 2 2 2 2 2 2 2 e 
    c e e 2 2 2 2 2 2 2 2 2 2 2 2 e 
    c e e 2 2 2 2 2 2 2 2 2 2 4 2 e 
    . e e e 2 2 2 2 2 2 2 2 2 4 e . 
    . 2 e e 2 2 2 2 2 2 2 2 4 2 e . 
    . . 2 e e 2 2 2 2 2 4 4 2 e . . 
    . . . 2 2 e e 4 4 4 2 e e . . . 
    . . . . . 2 2 e e e e . . . . . 
    `, SpriteKind.Player))
myApple.pen(TurtlePenMode.Up)
myApple.moveDirection(TurtleDirection.Backward, 50)
myApple.pen(TurtlePenMode.Down)
for (let index = 0; index < 4; index++) {
    myDuck.moveDirection(TurtleDirection.Forward, 25)
    myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
}
for (let index = 0; index < 4; index++) {
    myApple.moveDirection(TurtleDirection.Backward, 25)
    myApple.turnDirectionByDegrees(TurtleTurnDirection.Left, 90)
}
```

## Step 10
** Try it Out**

You can use the previous example to draw a circle! If you turn a small amount of degrees many times over, you will eventually end up back where you started. The first 7 blocks just move the **Turtle** to not be in the center of the screen.
```blocks
let myDuck = turtle.fromSprite(sprites.create(img`
    . . . . . . . . . . b 5 b . . . 
    . . . . . . . . . b 5 b . . . . 
    . . . . . . b b b b b b . . . . 
    . . . . . b b 5 5 5 5 5 b . . . 
    . . . . b b 5 d 1 f 5 5 d f . . 
    . . . . b 5 5 1 f f 5 d 4 c . . 
    . . . . b 5 5 d f b d d 4 4 . . 
    . b b b d 5 5 5 5 5 4 4 4 4 4 b 
    b d d d b b d 5 5 4 4 4 4 4 b . 
    b b d 5 5 5 b 5 5 5 5 5 5 b . . 
    c d c 5 5 5 5 d 5 5 5 5 5 5 b . 
    c b d c d 5 5 b 5 5 5 5 5 5 b . 
    . c d d c c b d 5 5 5 5 5 d b . 
    . . c b d d d d d 5 5 5 b b . . 
    . . . c c c c c c c c b b . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player))
myDuck.pen(TurtlePenMode.Up)
myDuck.moveDirection(TurtleDirection.Backward, 7)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Left, 90)
myDuck.moveDirection(TurtleDirection.Forward, 40)
myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
myDuck.pen(TurtlePenMode.Down)
myDuck.setPenColor(8)
for (let index = 0; index < 120; index++) {
    myDuck.moveDirection(TurtleDirection.Forward, 2)
    myDuck.turnDirectionByDegrees(TurtleTurnDirection.Right, 3)
}
```

## Step 10
**Success!**

You can now use loops, to make your code more efficient.

## Step 11
**Your Turn**

Get your **Turtle Object** to draw a red octagon (a stop sign). Remember in a regular octagon there 8 sides and all the angles are 45°.
![octagon](https://github.com/Mr-Coxall/makecode-arcade-turtle-logo-lesson6-advanced/raw/main/assets/octagon_screenshot.png)

**BONUS**

Get 2 **Turtle Objects** each drawing an octagon (a stop sign).
![octagon](https://github.com/Mr-Coxall/makecode-arcade-turtle-logo-lesson6-advanced/raw/main/assets/octogon_two_objects.png)

## Step 12
**Done**

You have successfully completed your six lesson in Turtle Logo.

```ghost
let myTurtle = turtle.fromSprite(sprites.create(img``, SpriteKind.Player))
myTurtle.moveDirection(TurtleDirection.Forward, 0)
myTurtle.turnDirectionByDegrees(TurtleTurnDirection.Right, 90)
myTurtle.setPenColor(0)
myTurtle.pen(TurtlePenMode.Up)
myTurtle.say("Hello, World!")
for (let index = 0; index < 4; index++) {
}
```
