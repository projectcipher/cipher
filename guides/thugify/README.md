# Guide Three: Thugify

![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449360069524_giphy.gif)
##Introduction
###What is Thugify?
**Thugify** is an introduction to the **basics of Javascript + jQuery.**

We'll be adding **", dawg"** to the end of whatever you type into **an input box** — simple, but sweet.
* You'll be able to change the word added at your own will.
* You can customize this to make it Politify, which adds **",please"** instead

This **slide deck** created by Amy Sorto and modified by [Cipher](http://projectcipher.io) is a great introduction to key concepts. Please take a look through it [here](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit)!

###Resources
 Code: https://ide.c9.io/jevinsidhu/thugify 
 Final Webpage: http://jevinsidhu.github.io/thugify

##HTML
###Setting Up Your Files and HTML Document
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
![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449367351294_giphy.gif)

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
  <h1 id="title">Thugify</h1>     
</div>
```

**3. Let's create a place to input our text with the `<input>` self-enclosed tag**

`<input>` is a **self-enclosed tag** for creating an **input box.**

We'll be able to type in this box!

![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449368504615_Screen+Shot+2015-12-05+at+9.21.34+PM.png)

Give this input box an **id of "texter"**
`<input id="texter">`

We can give the box **"placeholder text"** as well~
* Placeholder text is the greyed out text (see the picture above)

Add a **`placeholder` attribute** (like `src` is an attribute);
* `placeholder="some text"` *right after the id*

`<input id="texter" placeholder="insert text">`

*We've made the place holder simply say "insert text"

**4. Let's make as ubmit button with the `<button>` tag**

`<button>` is the tag for creating a button
* Just like the `<h1>` tag, this is another tag where we place text between the opening and closing tags to display on the webpage

Give this button the **text "thugin'"**

```<button> thugin' </button>```

Give this button an **id of "go"**

`<button id="go"> thugin'</button>`

We're going to tell the webpage that this is of **type-something**
  * In this case, it's a **button**!

*To do this, we're also going to give this a **`type` attribute**

Another one (**attribute**);

[Broken Youtube Link Here]

* type="button" *right before the id*
  * This is to ensure that the webpage understands we want a button
   * By specifying this, the HTML adds some build-in CSS styling

```
<div class="thugin"> 
  <h1 id="title"> Thugify</h1>  
  <button type="button" id="go"> thugin'</button>   
</div>
```

###*Look at that beautiful indenting. Is yours indented?*
![](http---i.imgur.com-qHEIc0k.gif)

**4. To create a space for our thugified content, let's create a `<p>` tag with an id of `output`**

`<p id="output"> </p>`

`<p>` stands for paragraph
* Just like the `<h1>` tag, this is another tag where we place text between the opening and closing tags to display on the webpage

Whatever text we type into the **input box** will have **", dawg"** added
* We will then add the text between the opening and closing `<p>` tags
  * We'll do this using **JavaScript**

Final Code (**do not copy and paste, you bumface**);
```
<body> 

<!-- Our main HTML -->
  <div class="thugin"> 
      <h1 id="title"> Thugify </h1>
      <input id="texter" placeholder="insert text">
      <button type="button" id="go"> thugin' </button>
      <p id="output"> </p>       
  </div>
  
<!-- Our JavaScript files, also referred to as simply "scripts" -->  
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="script.js"> </script>
  
</body>
```

##CSS
CSS (cascading style sheets) is the styling of our page
* This styling lives in the **style.css** file

We use selectors in CSS that select our HTML tags

We want **you** to style the page!
* If you feel uncomfortable, that's good! You'll only really grow by being put into uncomfortable situations and then figuring your way out

* Your peers are **here to help you** if you have any questions, **all you gotta do is ask**
  * **Google** is also amazing! it's what ***all programmers*** turn to, especially **professionals**!

If you feel completely lost, no worries! Go back to our older workshops and skim through those (linked at the top of this document).

###We the best; you can put the hinges in the hands.
https://www.youtube.com/watch?v=skY-FKgOIew

##Javascript + jQuery, dawg
Remember that the variable names in the examples below can be **anything** you want, but we recommend sticking with ours in order to make the workshop easier to follow!

###Adding a Listener
To begin our JavaScript journey to *Thug Land* we'll need to add a listener to listen for a click on the **Thugify** button.
`document.getelementById('go')`
This line simply means: Find the element with the id "go" in the document.

Now we haven't done anything with this element yet, we want the button to trigger some code when someone presses it, so we'll add `.onclick = function() {}` to the end of the end of the line.

`.onclick` simply adds a rule to listen for a click on the button and runs whatever's behind it.
In this case, `= function() {}` happens to be assigned to it.

With that known, we can infer that `.onclick = function() {}` simply means: When a click is registered, run the following function.

To review, so far our code is
`document.getElementById('go').onclick = function() {}`
which simply says: Find the element 'go' and listen for a click on this element. ?If there is a registered click, run this function.

If you've followed along this far, awesome! You're doing great, we're almost done. If you're stuck, turn to a peer! We a team and we the best

.![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449382445802_5833673d42c72dd12cb4078eb757c92f.500x274x12.gif)

Now that we've gotten Javascript to listen for a click on the button, we need to tell it to do something when it gets a click.

###Creating a variable and Assigning a Value
Every line that we want to execute **needs** to be inside the curly brackets `function()`**`{}`**
Don't forget to indent it either! Remember, it'll make it easier to read.

So let's start with first finding what we need to **thugify.**

**Remember from [Slidedeck](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.gd76540ddf_0_22): When creating variables (var), whatever is on the right side, is always being assigned to the left side.**
* I.e. the content on the right is going to be assigned to the variable `div` on the left

**The id `texter` is from the input box!**

We'll be grabbing the value from the input box, since the id `"texter"` is assigned to the box
* Whatever someone types into the input box will be retrieved with this line of JavaScript

To do that we need to use:
`var div = $('texter').val();

WOAH HOLD UP DID YOU SEE THAT?????
LOOK AGAIN.

![](http---i.imgur.com-EQiLdKF.png)

You're probably wondering what the heck that `$` is doing here. Remember the libraries section in the [Slidedeck](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.gd76540ddf_0_22)?

That's the **power** of **jQuery** at work. 

It took something we would normally use like
`document.getelementById('texter')`

And shortened it to:
`$('#texter')`

Of course `document.getelementById('')` would still work if you'd prefer that.

![](office.gif)

Note: It finds HTML elements exactly like a CSS selector would:
* ids would be: `#[id]`
* Classes would be: `.[classname]`
* Regular tags would work too: `$('h1')`

Therefore:
`var div = $('#texter')`

Means the same thing as:
`var div = document.getElementById('#texter')

Place `.val();` at the end of the line
* Takes the value of whatever's behind the `.`

So to clarify everything:
`var div = $('#texter').val();`
Means to take the **value of** the element **`texter`** and **store it into a new variable** called **`div`**

We're grabbing the value from the input box, since the id `"texter" is assigned to the box
* Whatever someone types into the input box will be retrieved with this line of JavaScript.

We're gonna use this ***string*** value to thugify later on.
* A string is a series of characters (text and numbers!)
  * This is also mentioned in the [Slidedeck](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.gd76540ddf_0_22)

So, we've debunked that msyery!

![](mystery.gif)

Let's move on to performing the actual **thugifying** part of the string we got in the last part. 🏀

###Adding the `", dawg"` to the `add` Variable
We need to store the variable with the words from the input box and then **add** the word `", dawg"` to it

`var add = div + ", dawg";`
This line takes the tsring we got in the last section (variable div) from the input box, and adds `", dawg"` to the end of it, and then stores it into a new variable named `add`

Adding the two strings together is called `Concatenation.` Ya fancy, huh?

![](steveharvey.gif)


Alrighty, now that we're **thugin'** it's time to display our up text on the page — fo'shizzle.

###Displaying the Text
We're going to use `document.getelementById()` to find an element on the HTML page by it's id

` document.getelementById('output')
This will take care of that job for us
* We're finding the element with the id `output`

**PS:** you can use jQuery's `$('')` for this as well since there's practically no downside.
* Try changing this line to use the jQuery syntax
  * Syntax means the grammar, spelling and set of rules of a language

Now then, we will attack `.innerHTML = add;` to the end of the line

`document.getElementById('output').innerHTML`

It's just like `$('#texter').val();` that we used before;
* Except this time we're setting the `innerHTML` value (the text inside the pairs of `<p>` tags) of an HTML element instead of getting a value from it.

Now we will assign the value of add to the `<p>` tag with the **id** `output`

`= add;`

In plain English, `document.getelementById('output').innerHTML = add;` means:
* set the `innerHTML` of `"#output"` to the value of the **variable**, `add` (our th*ugified string variable → the variable that holds our text*)

`document.getElementById('output').innerHTML = add;`

Close your curly brackets **(`}`)**, slap a semicolon **(`;`)** on the end of it and BAM you're done!

`};`

Final Code (**do not copy-pasta you bumface**):
```document.getElementById('go').onclick = function() {
    var div = $('#texter').val();
    var add = div + ", dawg";
    document.getElementById('output').innerHTML = add; 
};
```

##You are now a JavaScript Legend.

![](http://i.imgur.com/BJiD03Q.gif)

Unless you copy-pasted then ehhhh. Maybe a half-legend or something.

Your mom thinks you're special, that's all that really matters*

##Thanks for completing our workshop <3





