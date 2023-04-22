# Entry 5
##### 04/17/23

### How have I been learning my tool while building our MVP?
Although we have spent a lot of time learning our tool, but there was still some part that my partner, Angela and I have been stuck and don't have the solution to and had to do more research and tinkering through the kaboom website and Angela had watched tutorials to help her to go back to tinker and learn the parts that we still need help or the part that we are still need help on. This means that we were figuring out how I can add the score every time, the mouse touches a sprite. And how can I use this value to show and appear in the scoreboard. At first, I started with the code. I made a starting variable using `let` to help me set the value to 0. 
```js
let var score = 0;
// initial value

add([
    text(score),
    pos(0),
])
...
player.collides('bread', (b) => {
    destroy(b)
    score++
})
```
This code had add the score up behind the scenes, but not at the scene that is visble to the user and the player.
And when this code is activated,it doesn't show anything. I wonder what can we do. This had led me to the go back to [kaboom](kaboomjs.com) to see how I need to write the code to make sure that it works. After looking through the playground with the "scoreboard" section, I found out and learned that when I want to make the score from the scoreboard to increase, I would need to store the score inside a variable, similar to what we learn in js, and increase the score everytime when the mouse touches the sprite and the score increasing behind the scene, we would have to make the text change too, therefore, we would have to use `.text` to help us.
```js
let score = 0;
// score 
  
const scoreLabel = add([
    text(score),
    pos(0) 
])
...

// when the sprite collides with bread, the bread will disappear
// when the bread disappear, the scoreLabel will add 1
player.collides('bread', (b) => {
    destroy(b)
    score++  
    scoreLabel.text = score
})
```
We were CLOSE!!! This time after learning inside based of the kaboom property, we made the `add` property and stored it inside a variable, and everytime the mouse sprite collides with the bread sprite, I would have to add the score by one, and to change the score by making the `scoreLabel` to what is the current value of score.

### How have we been finishing our MVP?
My partner and I have done a lot to make out MVP to work. At first, we used all the sprites that we have drawn in [pixelart](pixelart.com/draw) to help me build the scene that the player will be playing in. First, we converted all the sprites that are loaded to a symbol in the key board and then, we changed their sizes and position. to make sure that they are the exact size compared to the whole scene, because some sprites are in different pixels and we used the property `scale()` to help us. If the value inside scale is < 1, then it will be smaller, and if > 1, it will be bigger. We also used `solid()` and `area()` to help to make sure that they don't move when the player is playing, so in this part, we had make the bush and the table to remain constant and don't move. Next, we used the `addLevel` property to help us build the level that we want by placing the symbols that we have converyed to. So we started our code as 
```js
const SPEED = 300 // speed of the sprite that is running in the game
    addLevel([
        "xxxxxxx          %    ", // x=bush
        "x      x    xxxxxxxxxx", // %=door
        "x       x!           x", // !=big mouse
        "x *      x    A      x", // *=cheese
        "x ^ =     x          x", // =little mouse
        "xxxxx      x   ^     x", // ^table
        "x      @    xxxxxx   x", // @=tomato sauce
        "x              =     x", // every symbol as shown can be repeated multiple times
        "x      ^ =           x",
        "xxxxxxxxxxxxxxxxxxxxxx", // fits the size of the computer and at certain points, we have to add the sprites that we have load and add
        ], {
        width: 60,
        height: 30,
        "x": () => [
            sprite("bush"),
            scale(0.79),
            solid(), 
            area(),
        ],
        ...
```
Next, to make our game work, we had to make sure that the player had to collect all the ingredient inorder to continue the next level. So, we had to give an `if-statement` that if the number is the same as 3, that is also the number of ingredients that the this level has. This also means that if we don't have the score or the all the number of ingredients collected, then the player won't be able to open the door and go to the next level of the game. Or if all the user had collected all the ingredients, then the user will be able to go through the door.
```js
// When the sprite collides with the door, it will go to the next level, when the sprite collected all the food
// If the sprite did not collect all the food, then the sprite can not go to the next level
    player.collides('door', (d) => {
    if (score == 3) {
        go("win")
    }
    }) 
```
Next, when this was all done, we were also to use the `go()` to help the user to go to the next scene. For instance, in the first level, they have to get all the sprites, and in the second level, there is a sprite in the beginning of the game. To make the game more interesting, we had make a sprite called "spike". if the user had touched the spike" it will bring the user to the next scene saying that "You have jumped on the spike" and when the user pressed backspace, then they will be restarting the second scene again.
```js
// when the sprite jump into a spike, it will say "You jumped into a spike"
add ([
    text("You jumped into a spike")
])

keyPress("backspace", () => {
    go("win") //scene 2 (player restarts)
})

// if the sprite jumps into a spike, it will bring them to the scene to where they lose 
player.collides ('dangerous', (q) => {
    go('lose') // scene 3 (where the player loses)
})
```
After building our scene, me and my partner believed that the game is to easy to pass because the `gravity()` is too low and that this had lead me to change the value of the gravity. Next, we made our own sprite and made it as the obstacles to the first level, and as mentioned before, the spikes were the obstacles that were for the second level. We made the mad mouse that the mouse have to jump over or to play over to get the ingredients. If the mouse runs into the enemy mouse, our code will function that the game has to restart. We got this inspiration from subway surf, and that the surfer had to run through the obstacles to get the coins and so what we did was to use that inspiration in our game to make our game more fun and more interactive.

### EDP
Now, we are in Step 5, creating a prototype of the EDP, the Engineering Design Process. After we finished learning our tool, we have been starting to use what we learn based of out tool to build our MVP, the minimum viable product - a product that is the bare minimum for our final product to work. We build an adventure game for the mouse, that they have to prevent themselves from touching the enemy mouse or else the player would ahve to restart the game again. After building the level, we have made the mouse to collect all the sprites in order to go into the next scene.

### Skills
Two skills that I have accomplished during doing and finishing our MVP (The Minimum Viable Product) are Collaboration and Debugging. First, it was "Collaboration" because it was during spring break, and me and my partner Angela had been working collaboratively and splitting up the work evenly through replit although we wern't able to see each other. When we had overcame an issue, we would have chat through messages and collaboratively solve the issue together. Therefore, this had helped me accomplished this skill of Collaboration and knwoing the importance of collaboration. This lead to "Debugging". Debugging comes up when me and my partner overcame this issue and was able to use `console.log()` to help me solve the issue. For instance, the whole time, we had our console opened, and when something doesn't work, the first thing that come to my mind would be using `console.log()` and it had helped me understand the syntax errors that I am missing when I open the console and it gave me a pathway to know where my mistake is and to solve this issue.

### MVP
 * [my MVP](https://freedom-project.angelal4844.repl.co)
 * [code to product](https://replit.com/@angelal4844/Freedom-Project#code/main.js)

### Sources
 * [kaboom](kaboomjs.com)
 * [pixelart](https://www.pixilart.com/draw)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
