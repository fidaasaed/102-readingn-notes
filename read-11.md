 # images
**what can you do in images ?**

* You can specify the dimensions of images using CSS. This is
   very helpful when you use the same sized 
images on several pages of your site.
* Images can be aligned both horizontally and vertically using CSS.
* You can use a background image behind the box created by any element on a page. 
* Background images can appear just once or be repeated across the background of the box.
* You can create image rollover effects by moving the background position of an image.
* To reduce the number of images your browser has to load, you can create image sprites.


![image](https://user-images.githubusercontent.com/79834102/112472309-a55da580-8d75-11eb-8b87-8107db664717.png)

![image](https://user-images.githubusercontent.com/79834102/112472384-bb6b6600-8d75-11eb-9d23-35d20ad2c079.png)


## Practical Info


Search engine optimization helps visitors find your sites when using search engines.
**give me an example for Analytics tools such as Google Analytics allow you to see how many people visit your site:**
* how they find it 
* what they do when they get there.

**what you need to To put your site on the web?**
you will need to obtain a domain name and web hosting.

*FTP programs allow you to transfer files from your local computer to your web server.
* Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website*
*tools (to save you writing them from scratch)*

![image](https://user-images.githubusercontent.com/79834102/112489098-cbd80c80-8d86-11eb-8318-f87cae1555c1.png)


## Audio
*I think we've taught you enough in this article. The HTMLMediaElement API makes a wealth of functionality available for creating 
simple video and audio players, and that's only the tip of the iceberg. See the "See also" section below 
for links to more complex and interesting functionality.*

**Here are some suggestions for ways you could enhance the existing example we've built up:**

* The time display currently breaks if the video is an hour long or more (well, it won't display hours; just minutes and seconds). Can you figure out how to change the example to make it display hours?

* Because <audio> elements have the same HTMLMediaElement functionality available to them, you could easily get this player to work for an <audio> element too. Try doing so.

* Can you work out a way to turn the timer inner <div> element into a true seek bar/scrobbler — i.e., when you click somewhere on the bar, it jumps to that relative position in the video playback? As a hint, you can find out the X and Y values of the element's left/right and top/bottom sides via the getBoundingClientRect() method, and you can find the coordinates of a mouse click via the event object of the click event, called on the Document object.*

** For example:**

**document.onclick = function(e) {
  console.log(e.x) + ',' + console.log(e.y)
}**
