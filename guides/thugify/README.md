# Guide Three: Thugify


##Introduction
###What is Thugify?
**Thugify** is an introduction to the **basics of Javascript + jQuery.**

We'll be adding **",dawg"** to the end of whatever you type into **an input box** — simple, but sweet.
* You'll be able to change the word added at your own will
*
You can customize this to make it Politify, adding **",please"** instead

This **slide deck** created by Amy Sorto and modified by [Cipher](http://projectcipher.io) is a great introduction to key concepts. Please take a look through it [here](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit)!

###Playlists
We are creating **playlists, recommended pathways** for our content -- this isn't the start of the content!

Try [this](https://docs.google.com/document/d/1jCkOlEbgu_mCJDYCEdBk-rUSqTicHQy8YutEJ5MM6mY/edit) first

Get it online using:
https://hackpad.com/Basic-Git-and-Github-gOQpi30cvG8

Try +Cringe 101 Workshop afterwards!

###Resources
 Code: https://ide.c9.io/jevinsidhu/thugify 
 Final Webpage: http://jevinsidhu.github.io/thugify

##Setting Up Your Files and HTML Document
1. Create a **index.html** file
2. Create a **style.css** file
3. Create a **script.js** file

If setting up your document is not familiar, please look at ++Cringe 101 Workshop.



This isn't 100% necessary for the code to run (it will still totally do so), but it tells the wbpage some key facts that make it **run without any hitches**

This should be placed in your *index.html* file

###Please do not copy and paste, you bumface:

```
<!DOCTYPE html>
<html>
  <head> 
    <link href="style.css" rel="stylesheet">
  </head>

  <body> 
  
    <script src="script.js"> </script>
  </body>

</html>```
```<script src="script.js">``` is **linking the HTML file to the JS file**
* Webpages + browsers are really dumb, humans just make them smart
* ```<script>``` is a tag that links the HTML file to the JavaScript file
 * ```src``` is called an **attribute**
   * It **specifies the location** — in this case it was simply the file name, *“script.js”* 

###NOTE: MAKE SURE YOU HAVE CLOSING TAGS
```<h1> </h1>```

##Adding jQuery
As mentioned in the [slide deck](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.p), **jQuery is a JavaScript library.**
* It adds functionality to the language, Javascript

Javascript was created in 1995 — that was 20 years ago (from 2015). We need libraries to keep the language **powerful and current.**

Using the same ```<script>``` tag we need to link the **content-delivery network (CDN)** for jQuery
*A **CDN** allows us to import a file that contains the jQuery library.
 *If you open https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js, it is a bunch of lines of code! 
 
* You could download this, include it alongside your files, and link the file name instead of the CDN URL. It would be same as using a CDN.
 * CDNs simply allow us to have the same functionality quickly. 

**Include the linking of jQuery above your ```script.js``` file**

* HTML runs top-to-bottom
* The jQuery should come before the script.js file, so it can leverage its power
 * Remember, HTML runs top to bottom. We need the jQuery to be read first.


```<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>```<br/>
```<script src="script.js">```

##Creating the HTML Structure
Our focus for this workship is the basics of **JavaScript + jQuery.** Let's finish up our HTML first!
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449367351294_giphy.gif&hmac=1IhuTT125HusbBGoBdgbggzj8q5reMqtRDFA%2F0uISFo%3D)
**Note: All of this must be enclosed by the `<body>` tag. The closing tag, `</body>`, should be after your script tags.**

###[Let's go](https://www.youtube.com/watch?v=AYD4dZqCpdU&feature=youtu.be&t=17)
[Please ~~don't~~ turn up that hard to our workshop]

**1. To enclose our content, we'll create a `<div>` tag**

This is a container to:
* Organize our content
* Apply styling from our **style.css** file to everything enclosed

```
<div class="thugin">

</div>
```

**2. To add the name of the workshop, let's create a `<h1> </h1>` header tag**

Give the header tag an id of "title"
* Type `id="title"` before the `<h1` is closed

It should look like this: `<h1 id="title"> Thugify </h1>`

* I.e. there may be multiple `<h1>` tags in your code
* To select one it needs to have its custom name, thus the id

Indent your code!
* Indenting items that are enclosed within another tag is important for your own readability
  * In this case `<h1>` is enclosed in `<div>`
```
<div class="thugin"> 
  <h1 id="title"> Thugify</h1>     
</div>
```

**3. Let's create a place to input our text with the `<input>` self-enclosed tag**

`<input>` is a **self-enclosed tag** for creating an **input box.**

We'll be able to type in this box! ![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449368504615_Screen%2BShot%2B2015-12-05%2Bat%2B9.21.34%2BPM.png&hmac=5cgxe%2FdXpjqTSlOwbuuYVcml%2Fd4%2FGBitHdDnVr6wbKk%3D)

Give this input box an **id of "texter"**
`<input id="texter">`

We can give the box **"placeholder text"** as well~
* Placeholder text is the greyed out text
















