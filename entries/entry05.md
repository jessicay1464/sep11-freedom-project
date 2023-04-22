# Entry 5
##### 04/17/23

### How have I been learning my tool while building our MVP?
Although we have spent a lot of time learning our tool, but there was still one part that I still went back to do and learn. This was figuring out how I can add the score every time, the mouse touches a sprite. At first, I started with the code 
```js
let var = 0;
// initial value

add([
    text(score),
    pos(0),
])
...

score++
```
However, when this code is activated, it shows an error. This had led me to the go back to [kaboom](kaboomjs.com) to see how I need to write the code to make sure that it works. After looking through the playground with the "scoreboard" section, I found out and learned that when I want to make the score from the scoreboard to increase, I would need to store the score inside a variable, similar to what we learn in js, and increase the score everytime when the mouse touches the sprite and the score increasing behind the scene, we would have to make the text change too, therefore, we would have to use `.text` to help us.
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
const SPEED = 300
  addLevel([
            "                      ",
            "xxxxxxx          %    ",
            "x      x    xxxxxxxxxx",
            "x       x!           x",
            "x *      x    A      x",
            "x ^ =     x          x",
            "xxxxx      x   ^     x",
            "x      @    xxxxxx   x",
            "x              =     x",
            "x      ^ =           x",
            "xxxxxxxxxxxxxxxxxxxxxx",
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
Next, to make our game work, we had to make sure that the player had to collect all the ingredient to finish the game. So, we had to give an `if-statement` that if the number is the same as 3, that is also the number of ingredients that the this level has. This also means that if we don't have the score or the all the number of ingredients collected, then the player won't be able to open the door and go to the next level of the game. Or if all the user had collected all the ingredients, then the user will be able to go through the door.
```js
// When the sprite collides with the door, it will go to the next level, when the sprite collected all the food
// If the sprite did not collect all the food, then the sprite can not go to the next level
    player.collides('door', (d) => {
    if (score == 3) {
        go("win")
    }
    }) 
```

### EDP
Now, we are in Step 5, creating a prototype of the EDP, the Engineering Design Process. After we finished learning our tool, we have been starting to use what we learn based of out tool to build our MVP, the minimum viable product - a product that is the bare minimum for our final product to work. We build an adventure game for the mouse, that they have to prevent themselves from touching the enemy mouse or else the player would ahve to restart the game again. After building the level, we have made the mouse to collect all the sprites in order to go into the next scene.

### Skills
Two skills that I have accomplished during doing and finishing our MVP (The Minimum Viable Product) are Collaboration and Debugging. First, it was "Collaboration" because it was during spring break, and me and my partner Angela had been working collaboratively and splitting up the work evenly through replit although we wern't able to see each other. When we had overcame an issue, we would have chat through messages and collaboratively solve the issue together. Therefore, this had helped me accomplished this skill of Collaboration and knwoing the importance of collaboration. This lead to "Debugging". Debugging comes up when me and my partner overcame this issue and was able to use `console.log()` to help me solve the issue. For instance, the whole time, we had our console opened, and when something doesn't work, the first thing that come to my mind would be using `console.log()` and it had helped me understand the syntax errors that I am missing when I open the console and it gave me a pathway to know where my mistake is and to solve this issue.

### Sources
 * [kaboom](kaboomjs.com)
 * [pixelart](https://www.pixilart.com/draw)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
