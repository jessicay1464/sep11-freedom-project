# Entry 2: Learning my Tool
##### 12/12/22

Connecting back to the last blog, my tool is "[Kaboom](kaboomjs.com)".
During November 14th, I started setting up my tool for [KABOOM](kaboomjs.com). But before that I started learning how some basic components work. I went to Kaboom's actual website to find out about the starter code and paste it into my ide. And I started my coding into it based on the documentaries that I learned. Although some failed, but I would have to debug and solve the issue.<br>
Starting November 28th, I learned my tool by watching through the YouTube tutorials and reading through the documentaries listed down below in "SOURCES". But before actually tinkering with my tool, I needed to make sure that I understood each part. Therefore, I started reading through the documents in the [KABOOM](kaboomjs.com) payground and taking notes in my SEP 11 notes by doing bullet points and understanding what  the different property will work. Such as
 * `pos(x,y)` //the position of "text" and "sprites"
 * `text()` //renders text
 * `sprite()` //sprites images itself
 * `add([])` //can render both texts and sprites
 * `rotate()` //rotates the sprite
 * `loadSprite()`// it helps load a sprite
The differnce between a `add` and `load` is that `load` is similar to calling after you `add` it.<br> 
Adding on the `pos(x, y)`, it randomly selects a postion unless you provide an actual number or value. Adding on, `pos (center())` makes the sprite in the center.<br>
I also learned the code of 
```js
onKeyDown("left", () => {
player.move(-SPEED, 0)
})
onKeyDown("right", () => {
player.move(SPEED, 0)
})
onKeyDown("up", () => {
player.move(0, -SPEED)
})
onKeyDown("down", () => {
player.move(0, SPEED)
})
```
I learned that this is the code that `onKeyDown` was that the code that could help the user to use the arrow keys that could help the sprites to move left, right, up, and down. I had also changed the values in the `player.move()`, and I learned that the lower the number, the slower the sprite would go, and the higher the number, the the faster the speed.<br>
Another important property that I have learned was 
```js
const level = addLevel(LEVELS[levelIdx || 0], {
    width: 64,
    height: 64,
    pos: vec2(100, 200),
    "@": () => [
        sprite("bean"),
        area(),
        body(),
        origin("bot"),
        "player",
    ],
    "=": () => [
        sprite("grass"),
        area(),
        solid(),
        origin("bot"),
    ],
    ...
    })
```
In this code above, I learned that we can convert into a code into a symbol. It would be much efficient than writing the link over and over again, espacially when you want to repeat the sprite multiple times. I learned that with this symbol, we can build out our own sprite and own game and make a scene out of it. It would then come out of a scene such as 
```js
    [
		"@  ^ $$ >",
		"=========",
	],
	[
		"@   $   >",
		"=   =   =",
	],
]
```
With what I learn now, I have been only using the sprites inside the [Kaboom](kaboomjs.com) website itself. In the example above, each bracket inside means their own scene, so in level one, if the user passed level one, they would then go to level two, that is also the second bracket. This also notify the idea of `scene` and `level`. Later on, I would learn and make my own sprites and import it to my tinkering. 

#### My Goals for Winter Break
During winter break, I want to spend more time with my family and friends and also have a good rest and not think about homework for a few days. I hope that I can use my time to catch up in any missing lessons, not only on Javascript (SEP 11) but my AP classes during this ten day break. I also want to use this time to improve myself in certain skill such as reducing the amount of procastinating and using my time wisely ad making myslef mre productive, such as spending more time outside than at home.

### Skills
During this part of my project, I learned many components based on [Kaboom](kaboomjs.com) and how they work and how it would help me throughout this project on constructing this project. Therefore, I learned many skills. For instance, some skills that I have learned was `collaboration` and `attention to detail`. <b>Collaboration</b> was because of how the idea that when I was laerning my tool, and I was having problem with setting up my code, I asked my friends to help, and we worked out with this process together. To add on, another skill that I have learned throughout this process was <b>Attention To Detail</b>. This was because when I was using Kaboom to write my own code in my ide workspace, I have forgot to add a `)` that had cause my code to run into an error. Futhermore, this had also help me gain the skill of `debugging`. Being able to fix the conflict with my code.

### Engineering Design Process (EDP)
Learning how to use my tool is in the process of `Reseaching the Problem`.  After being able to know what tool I was gonna use, I had to break down into smaller parts and understand the components and how it can be inputed in my project. And connected to my topic on the "Adventure Game". Coming across with idea that I don't know, we would have o carefully read over the documents and ask for help. With the idea that we can also use google and research issues and getting idea on how to fix the code was also a great way to learn and reseach on how to use your tool.

### SOURCES
 * [KABOOM](kaboomjs.com)
 * YOUTUBE [video](https://youtu.be/4OaHB0JbJDI) on setting up --> but later use the setting up code from kaboom website itself.
 * KABOOM [playground](https://kaboomjs.com/play?demo=add)

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
