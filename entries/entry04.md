# Entry 4 Building MVP
##### 3/13/23

 After last time, after doing some deep tinkering of my tool, I learned many concepts about creating sprites, loading sprites, movements, background...etc. After, I learned that many different parts of the concepts were not as challenging, but the most challenging part was that connecting the scenes together was the most challenging because, it was confusing on how the code should be connected to each other. For instance, the idea of using `go()`. I have been wondering, where can this code be applied in the whole code? Should it be inside or outside of the curly brackets? What will I see when this code is writtened here?
 <br>
 How can I start my MVP? Well, I was thinking, we can start building one scene at a time, but how? It was difficult to imagine where should this sprite be placed and where can this sprite be found or should we created one? Although, I know how the many different code works, but we don't actually have our layout on what and where should each code and sprite should be placed on the screen. UP? DOWN? LEFT? RIGHT? Well, inside of our plan, we needed a day to draw a layout of what the code should be looked like. After communicating with my partner Angela, we decided to draw our own sprite. And on a computer paper, we decided to draw out our plan and for each sheet of a scene, we decided to include different scene. This was significant because, we were able to dump out our ideas into the paper. Also, since our project idea was based on adventure, we needed to make obstacles.<br>
 First, using the link called [PixelArtMaker](http://pixelartmaker.com/) and it seems that I wan't able to save my progress. the next day, I asked my other classmates the link that they were using and there, they introducing me to [PixelArt](https://www.pixilart.com/draw). This was way more useful because I was able to save my progress anytime. Next, for better collaboration with me and my partner, I created a repository that made it easier for me to connect with the code of us and also we can git push and pull much more easier with our code.
 We were to make and create our first scene. First, as a placeholder, we went online to find images that we can used as sprites, and we decided for beyond MVP to continue drawing out the sprite creating out project and its animation. After that we continued adding and loading sprites as shown here
 ```js
loadSprite("background2", "img/background2.png"); // bakcground color for level 1
loadSprite("block", "img/block.png"); // bakcground color for level 2
loadSprite("egg", "img/egg.png"); // bakcground color for level 3
loadSprite("cheese", "img/cheese.png"); // bakcground color for level 4
loadSprite("flour", "img/flour.png"); // main character
loadSprite("tomato", "img/tomato.png"); // main character
```
After we continued our loading sprites, we added movements to our project by using
```js
onKeyDown("left", () => { // sprite go left
player.move(-SPEED, 30)
})
onKeyDown("right", () => { // sprite go right
player.move(SPEED, 15)
})
onKeyDown("up", () => { // sprite go up
player.move(30, -SPEED)
})
onKeyDown("down", () => { // sprite go down
player.move(15, SPEED)
})
```
When we had add movements, we had created a first scene and basic scene to see how it functions and how it works. We found out that this was challenging because when we needed to add the second scene to make the basic game more interactive for the user, but there was an error to the code and we had debug it by using `console.log()`. It was confusing where the `go()` should be placed. This was significant because although I thought that I knew many concepts of kaboom, it was still very difficult to know where the code should belong `go()`. 

### How I was learning my tool
When me and my partner found that it was difficult to find where the code should be placed and it was difficult, i decided to go back and learn this part of my tool. I also went back to look at tutorials at how other programmers had used `go()`, and it was difficult to find because the video had used many `go()` and I didn't know which was best suitable for me in this case. I was learning this part of my tool by copying and pasting my code into jsbin to see the output and to tinker with it around to see how it works when in different areas. And this was my part that I am learning right now and to be done. 

### Skills
Two skills that I have accomplished mainly while in this building of MVP were Problem Decomposition and Communication. Hence, the first skill that I have learned was Problem Decomposition was because while creating my MVP/prototype, there are still many concepts that I still have not been very familiar and I would have to slowly break down the problem that I have so far and research the issue that I have so far and fix the conflict. Next, was communication, and this was because i have a partner and with communication, we were greatly able to commmunicate and seperate and learn the work together. With things that I don't understand, she might understand, so in this case, communication was very relevant when contributing to the project. But also, not only communicating with my partner, but also when I am creating my own sprites, I have asked other classmates using the same tool, KABOOM as me to help me such as introducing to me to the pixelart linked in the bottom that had helped me a lot too.

### EDP
I am now in the middle of the process of <b>Researching the problem</b><b>Plan the most promising solution</b>, <b>Create a prototype</b>. First of all, I say I was still researching the problem because I was creating the prototype, my MVP, I was still looking up the issues that I was having in [Kaboom](kaboomjs.com), reseaching the tiny issues that I had missed out accidently that can help me throughout the process of building up my code. Also, I also added in planning the most promising solution because me and my partner Angela, was also making a planning out on paper on how out project would look like and drawing out the scene, it was a part of our planning. Lastly, I was also saying creating a prototype because this time, we are in the process of creating a MVP, the Minimum Viable Product. This was a part of me and my partner in the process of making a product or the prototype. 

### Sources
 * [Kaboom](kaboomjs.com)
 * [PixelArt](https://www.pixilart.com/draw)
 * [PixelArtMaker](http://pixelartmaker.com/)



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)