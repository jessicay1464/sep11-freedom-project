# Entry 3 Tinkering with Tool
##### 02/06/23

During this part of tinkering of my tool, it was a continuation from last tinkering. I learned to `add()` sprites, `loadSprite()`sprites, `pos(x, y)` sprite, how to apply a sprite with its symbol such as `@, #, %, ^, &, * ...`. Learning these basic codes of kaboomjs, it had helped me with building scenes later on.
```js
[
	"@  ^ $$ >",
	"=========",
],
```
I learned that after using a `[]` can help us build one scene and by building what's inside it by how we convert the the sprite to symbols, we can start building the scene.<br>
But not after, I found out a problem with the output itself, I should need to change the background and not let it keep as the default background. So I went onto a link on youtube that my partner had introduced me to. After watching it, I found out that there wasn't any specific code to specify the code, but it's actually just an image that has been put large and behind everything. Therefore, I was adding the image of a background to my code, however, it appears how the code was working, but the pixels were not just full screen, and that it was difficult to know hoe to change the background of the code because it deoesn't specify how to chnage the bakcground of the code, therefore, I would have to add code that specifically changes the background, what I can do is import and image, and select the `img` and set the length and the width of the image. This is how it would look. 
```js
{width: width(), height: height()}
```
At first, I only imported the width, but it only shows the width of the image being full width, but the length of the image hasn't been changing. And so, I was creating a issue, as I continue watching the video, I continued watching the video and that help me to understand to add the `length: length()` back in. But this had once again opened up my curiousity, "Why isn't there any values inside the parentheses?" So immediately, I typed in a wildly large number 300, thinking it would change my image a lot, but actually, it did. It made my image smaller. As tinkering, it made me understand that without a number, it would change the length and the width to its default, the largest it can be, the screen size, but also that when you import a number, it would go with the `number imported + px`.<br>
After getting that done, I went to discover scenes. `Scenes` are relatively imporant in this case because of the idea how it can make the game more fun and interesting and more interactive. As scrolling through the website itself, i scroll through the code and found `if-statements`
```js
layer.onCollide("danger", () => {
	player.pos = level.getPos(0, 0)
	// Go to "lose" scene when we hit a "danger"
	go("lose")
})
```
Over here, I learned that when the position of the sprite gets to a certain area in a code, it would say to `go("lose")`. When it loses, it would go to another scene. So I also learned that the `go()` activated the scene to go to lose. The `"lose"` was the second scene that was created by the user. But I wonder how can we connect the two scenes together? Such as where should I place the `go()`. I would have to do further tinkering to help me. 

```js
player.onCollide("coin", (coin) => {
	destroy(coin)
	play("score")
	score++
	scoreLabel.text = score
})
```
An a-ha movement that I found while I was tinkering and reading through the code/documentary was that it is so similar to the code that we have been learning in class about the `javascript`. Such as the structure, such as the increment of a variable,a nd the idea of overwriting code. Similar to the `DOMS` that we have been learning so far.<br>
To conclude, throughout tinkering, I have met many challenges inside codes,a nd we would have to slowly debug it to help us to understand and get the code better and better.

### Planning on learning next
The next concept that I would learn is how to build and connect the second scene together or multiple scene together. Since now, I know how to create one scene, it would be fun and interesting to create the next one. For instance, if I would want to create a scoreboard at the end of the game, it would bring the user there, but if the user loses, it would bring to the scene to "YOU LOSE" an the button for try again. Therefore, it can make the game more interactive. Furthermore, I would like to add on how I want to learn how we can connect the keys on the keyboard to control the sprites added and uploaded on the screen. As if, "How can I connect this together?" I learned most of the small pieces, so how would I connect the "little pieces" together.

### Skills
Two skills that I have learned while tinkering with my tool is collaboration and debugging. Collaboration was because when I was having difficulties with my lengthing out my project background. But I wasn't able to found out why it doesn't work after going through [kaboom](kaboomjs.com) website itself and researching in google. Therefore, I went to ask help for my partner. This was much helpful because she had also met the same issues as me before, when she was having difficulties with this issue, she went through tutorials that had helped her. So when I was having the same issue, I was able to ask for her help and she was able to collaborate with me and that helped me with debugging my issue. This leads me to debugging. I was having a tiny error with the code that made my whole output become an error. This was because I forgot a `}` after the parentheses, and this had lead me to help me use `inspect`, and this had lead me to find my error and fix it.

### EDP (Engineering Design Process)
Now, I am still on the step of "Researching the problem." This was because I am still learning my tool and how to use it. As from before, I know what my tool is, and I was able to define my problem, I am still in the process of learning on how my tool should work and learning the differnt concepts about it. Also, when coming across the code or concept that I didn't understand in the code before, I would have to research on google, or even ask for help cause in the website, we would have to come up with issues, but there isn't any explanations, but just a code and how it works, so it would be very helpful to have videos and different sources to help us with something when we don't understand it.

### Sources
 * [Flappy Bird](https://www.youtube.com/watch?v=hgReGsh5xVU)
 * Building [Scenes](https://kaboomjs.com/play?demo=scenes) with kaboom

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
