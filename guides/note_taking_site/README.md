
# Tools for Making a Note Taking Site

## Introduction

### What is this Workshop?
This workshop will give you **tools** you can use when creating a note taking site. We want **you** to make your own!

### Examples of Blogs

Curated by [Jevin](https://twitter.com/jevinsidhu), here are good examples:

* [Svbtle blog](https://jevinsidhu.svbtle.com/)
* [Jevin's black-history blog](http://jevinsidhu.github.io/black-history/index.html)
* [PM Archive](http://pmarchive.com)

Here is a good example of what you'll be able to make with these tools:

[Finished note taking site](https://preview.c9users.io/jevinsidhu/firebase-tutorial/index.html)

## Setting Up Your Document
1. Create a *index.html* file
2. Create a *style.css* file
3. Create a *script.js* file

Ensure your *index.html* initial structure should look like this:
```
<!DOCTYPE html>
<html>

  <head> 
    <link href="style.css" rel="stylesheet">
  </head>
  
  <body> 
    <script src="script.js"> </script>
  </body>
  
</html>
```

Its good to keep this initial structure in a new file called *structure.html* so you can copy and paste this whenever you start a new work-space or create a new html file.

## Tool 1: Text Styling

These are some tips for styling your text:

1. 
 **Line Height**

Line height is a CSS **property** that specifies the line height of text. 

**What is a property?**
**A property** is the **key** in a **property-value relation**:

* **Property** is what you want to change
  * Line height
  * Color
* **Value** is by how much
  * 10px
  * 100%

**Example:** The first picture is without line-height. The second is with a line height of "1.7".
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456435946944_Screen%2BShot%2B2016-02-25%2Bat%2B4.32.14%2BPM.png&hmac=Bbr3Rbs0hyANGT7qb1thSeiqP1CLDW7U%2FfMj%2BWzu6Rg%3D)

![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456435941269_Screen%2BShot%2B2016-02-25%2Bat%2B4.32.02%2BPM.png&hmac=kE89sy3F6CaYCL8eQHPOHLUxc96TbHOY2tWsN%2B%2BjmGQ%3D)
```
.text {
  line-height: 1.7;
}
```
There is no units behind **"1.7"**. The unit is described as a **"number"**. Although you can place a unit behind 1.7 such as **"px"** too.

* Line height lets the text *breath* and is *convention* in design to have at least 1.5 line height between large chunks of text



2.** Antialiasing for Fonts**

Antialiasing will style the text to look more crisp and clear!

**Example:** The first picture is without antialiasing. The second one is with antialiasing.
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456437459603_Screen%2BShot%2B2016-02-25%2Bat%2B4.57.31%2BPM.png&hmac=RnlGqO7RtQXNYtwzhZUMcdwT61b7WagP7M3J%2BJn8bjY%3D)
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456437461382_Screen%2BShot%2B2016-02-25%2Bat%2B4.57.24%2BPM.png&hmac=vGXoZ24bZUZk6ozmPFPvqJEv3zWV4sVNUbEstLY3fEU%3D)

```
.text {
  -webkit-font-smoothing: antialiased;
}
```

**"Antialiased"** is the value in the key-value pair. The key is **“-webkit-font-smoothing”.**

**“Webkit”** is a web browser rendering engine for Safari/Chrome. 

* It extends our ability to style elements such as text with properties such as font-smoothing
* It is included right before a property as **“-webkit-”**

**"Font-smoothing"** is the part of the property, the key, in the key-value pair.

* Part of the CSS property that controls antialiasing when fonts are rendered.

3.** Color**

Black is the best color for large bodies of text usually.

* Color is the **property**
* The hex color, #000, is the **value**

Hex colors are denoted by a **"#"** and are followed by **3 or 6** characters.

You can find tons of beautiful hex colors of different colors on [Colour Hunt](http://colorhunt.co/)!

```
.text {
  color:#000;
}
```

Using an **off-black color** is also recommended! This lightens the black and increases the readability in some cases.

We can also use an **RGB value:**

* Another way of writing codes
* Gives even more color choices to choose from

It consists of:

* **Property:** color
* **Value:** rgb (red, green, blue)

The **1st** number changes the **red** value, the **2nd** number changes the **green** value, **3rd** changes the **blue** value

```
.text {
  color: rgb(51, 51, 51);
}
```

**Example:** The first picture shows the value: #000. The second shows the value: rgb(51,51,51):
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456439334719_Screen%2BShot%2B2016-02-25%2Bat%2B5.10.56%2BPM.png&hmac=CUX8DlGRcmPzMiIsMO38Kb5XM8eJgAHdFhvR7nJ%2FtIM%3D)
![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_7C75302283E950365E1EF85B8318A65AE9ECBDA5B873334EC939C14F9002A090_1456439348972_Screen%2BShot%2B2016-02-25%2Bat%2B5.10.46%2BPM.png&hmac=EeYRobyNqLyak%2BRrl3P0NO73YJ8j8EBuCpkq4Dcyzc4%3D)


4.** Text Width and Centering**

You might notice that your text spreads across the **entire** page — this can get a little hard to read so we need to fix that. Most blogs use tighter margins to make large bodies of text more readable. Check out examples on Medium or Svbtle. 

We can set the text width to whatever dimension (700px worked best in our case) by referencing the ```post-writing``` class.

The text would still be a little hard to read because it is to the far left of the page. We can adjust this by fixing up the margins. Set the left and right margins to ```auto```. Auto calculates the appropriate position between the left and right margins and centres the text. No need to mess around with numbers!

Set the margin on the top to ```3vh``` to space out the top of the text from other parts. ```vh``` is a unit of measurement in CSS3. ```1vh``` unit is relative to 1% of the screen the site is being viewed on. So if your screen’s width is 100 pixels in height, ```1vh``` would be equivalent to 1 pixel. If your screen’s height was 200, ```1vh``` would be equivalent to 2 pixels.

Your CSS for this particular class should look something like this:

```
.post-writing {
    width:700px;
    margin-top:3vh;
    margin-left:auto;
    margin-right:auto;
}
```

**Bonus**: Try changing the width from a pixel value to a percentage (change the number too, 700% would be way too big). Change your browsers window size and see what happens.

5.** Font**

A huge part of a note taking site or a blog is the writing -- it’s what you see. 
To make this beautiful we use fonts!

Changing your font is easy to do and **Google Fonts** ([https://www.google.com/fonts](https://www.google.com/fonts)) makes it even easier. There are hundreds of fonts Google offers to use for free on the site.

The best part about Google Fonts is that it gives you the code you need to put on your site. 

**Steps to add and change fonts:**


1. Navigate to google.com/fonts
2. Choose a font by clicking the middle icon (you can see more of the font details by clicking the 1st button → Scroll to go click the middle icon)
3. Fonts have **different weights** → Choose a few
4. This is just a fancy term for the thickness 
5. The numbers range from 100 to 700 in hundreds for a total of 7 ( some fonts have all 7 weights while some do not)
6. Go to the number 3 area where it says “Add this code to your website”
7. You’ll notice it looks exactly like a CSS file -- that’s because it is!
8. Since it’s a CSS file, you know what that means! Copy the code & paste in your head

Example of code in your head tag:

```
<!DOCTYPE html>
<html>
  <head>
    <link href='https://fonts.googleapis.com/css?family=Open+Sans' rel='stylesheet' type='text/css'>
  </head>
</html>
```

Now that we added the font, we can actually change our text to the font we like using CSS!

In the example below, we changed all the text to the desired font by using the property **font-family** on the body tag. 

```
body {
    font-family: 'Open Sans';
    color:#000;
    font-size:10px
    font-weight:300;
}
```


## Tool 2: Input Box

For the note taking site, there needs to be some type of **place** where you can **write your note**! To do this, we need a **text input box**.

We’re going to make a new page for writing your notes. 


1.** Create a new HTML file**
  * Give it the **same structure as your index.html** file meaning the head and body tags and links to fonts and the css file
  * Name is post.html
  
 
2.** Add a heading for the page**

Hint: ```<h1> </h1>``` tag


3.** Time to make the actual input box!**

To do this, we'll be using the ```<textarea>``` tag which creates a **box** in which you **can enter text!**

After the heading, add the code below to add a text box. Remember to give it a **class and id** so you can locate it in CSS and Javascript

```<textarea> </textarea>```

Check it out in the preview tab and try typing some text into it!

You’ll notice, it is pretty small at the moment and it looks quite ugly, but there’s many benefits!

The coolest thing about the <**textarea> tag** is that it **automatically adds a vertical scroll** so your text can be as long as you want it to be (basically **unlimited text**)!

Since it’s small at the moment, let’s **make it larger**! We can do this using **attributes**!

**Attributes provide additional information about an element**
   * They are always in the start tag of an element
   * Examples of attributes would be:
     * class
     * id

To make the **text box larger** we just need to **add** the **attributes of cols and rows** which affect the number of columns and rows respectively.

```<textarea cols="10" rows="50"> </textarea>```

Experiment with different column and row sizes to see which looks best!
 
 
You can add **placeholder text** so users can know what the box is for!
  * This is also accomplisshed through attributes!

**Google "How to add placeholder text"**


4.** Design the input box!**

The ```<textarea>``` tag is similar to any other html element meaning it **stylized using CSS**.

Some aspects you can design include the background color, border, font and font size. Use your creativity and make a beautiful and effective text input box!


5.** Title for your note?**

We’ve made the main text box where you write your note and have designed it, but we also need a **text box** where you can **write the title** of your note so you know what it’s about!

To do this, all you need to do is **literally follow the same steps you just did to make the text box!**

Just remember a few things when making it:
  * It should probably be above the main text box (**Order of code matters**)
  * It should probably be smaller than the main text box
  * Remember the all the **atributes** you can add!


6.** The Button**

Now that we’ve made our two text boxes, we need a button to press that will actually get the code running and realize that we are done writing our note.

To do this, we just need to use ```<button> </button>``` tag
  * Remember to give it a class!

```
<button class="submit-button"> HEY I'M A BUTTON </button>
```


### This is How Mine Looks! (It's beautiful ahlie)

![](https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fd2mxuefqeaa7sj.cloudfront.net%2Fs_B9A9DAF7C1EBE10B933D1C210C47B5F3FEFBE7640FC7DB44A88CF3DEF478045B_1456529591825_Capture.JPG&hmac=JkVfpsSnXl5ixHIdUVc4wyEvN63YTgpJF8jVlEGNb18%3D)

## YOU'RE DONE!

**Get it online using:** [Github Guide](https://hackpad.com/Basic-Git-and-Github-gOQpi30cvG8)


### Next week we'll leverage a backend with [Firebase](https://www.firebase.com/)!













































