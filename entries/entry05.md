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

### EDP
Now, we are in Step 5, creating a prototype of the EDP, the Engineering Design Process. After we finished learning our tool, we have been starting to use what we learn based of out tool to build our MVP, the minimum viable product - a product that is the bare minimum for our final product to work. We build an adventure game for the mouse, that they have to prevent themselves from touching the enemy mouse or else the player would ahve to restart the game again. After building the level, we have made the mouse to collect all the sprites in order to go into the next scene.

### Skills
Two skills that I have accomplished during doing and finishing our MVP (The Minimum Viable Product) are Collaboration and Debugging. First, it was "Collaboration" because it was during spring break, and me and my partner Angela had been working collaboratively and splitting up the work evenly through replit although we wern't able to see each other. When we had overcame an issue, we would have chat through messages and collaboratively solve the issue together. Therefore, this had helped me accomplished this skill of Collaboration and knwoing the importance of collaboration. This lead to "Debugging". Debugging comes up when me and my partner overcame this issue and was able to use `console.log()` to help me solve the issue. For instance, the whole time, we had our console opened, and when something doesn't work, the first thing that come to my mind would be using `console.log()` and it had helped me understand the syntax errors that I am missing when I open the console and it gave me a pathway to know where my mistake is and to solve this issue.

### Sources
 * [kaboom](kaboomjs.com)
 * [pixelart](https://www.pixilart.com/draw)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
