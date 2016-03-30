# Projects Section

*Time Estimate: 30 minutes*

Note: This is an extension to the [Personal Website](README.md) guide -- please complete that first before reading through this.

## Our Goal

This adds a project section to your personal site! It will look similar to this:

![Example site, project section](img/project_section.png)

Link to example website: http://jevinsidhu.github.io/workshop-website/

Link to final code: https://ide.c9.io/jevinsidhu/workshop-website

## Part One: Intro to Divs and Classes

1. Let’s hop back to our __index.html__ file for a little bit!
- We want to start to structure this document for our upcoming __project section__ 
2. We used __`<body>`__  tags to enclose all of our document, but we want to __divide that even further__ to outline a __landing section__ (your picture and name) and a __project section__
- The __`<div> </div>`__ tag defines a division or a section in an HTML document
3. In the CSS, we have been using __CSS selectors to select tags__
- What if you want to __call 1 of your 2 `<h1>` tags__ in your HTML → Both have the same selector right now.
  - To solve this and create __custom CSS selectors__, in HTML → This is called creating a __class__
- After __keyword__ (<div, <body, <h1, <head) of __any tag__, type __class=”class-name”__ to create a class
  - __`<div class=class-name”> </div>`__ 
  - These must no capitals and spaces are replaced by dashes 
4. __Create this div__ and name the class __“landing”__  and enclose the entire content inside of __`<body> </body>`__ 
- It is important to create names that make sense for the future for you to read and understand your code

`<div class=”landing”> |ALL CONTENT| </div>` 

![](img/divs_classes.gif)

## Part Two: Starting the Project Section

- Let’s start the project section with a __`<h1>` header tag__
  - This is the __same one we used for our name__
1. Create the `<h1> Projects </h1>` header tag 
  - Remember that the text inside the tags will be displayed to the page
2. Let’s __add a class__ to the tag, so we can do some special things in __CSS with its selector__
  - Remember: __class=”class-name”__ just after you open the `<h1>` tag
    - __`<h1 class=”project-title”>  Projects </h1>`__ 
      - I named the class “project-title” → descriptive and short, but __spaces must be dashes (-)__

![](img/project_section.gif)

## Part Three: h1 Class Styling

1. Head back to your __CSS__ and let’s style this h1 tag that has the __class “project-title”__
2. To __select the class__, you must __write a period (.) before__ the __class name__ 
- This lets the code know that this is a class and not a tag like `<body>` or `<h1>` or `<img>` 
3. We’ve aligned text into the center before → __Let’s left align it.__
- Look at your previous code written to center your body → use the same but replace “center” with “left”
- This code overwrites the center aligning from the __CSS body selector__  because it is lower on the document remember the computer reads __HTML and CSS run top to bottom__ 

![](img/h1_stylin_proflin.gif)

- Kind of like our photo with the top of the webpage, __“Projects” is too close to the left side of the webpage__
  - We __fixed that with margin-top last time__ → This time let's use __margin-left__
- __Look at your past code with margin-top → Copy & Change -top to -left and a value of 250px is solid__
  - Feel free to play around with the value to see what look good to you

![](img/h1_stylin_proflin2.gif)

## Part Four: Creating the Projects / Items 

1. Let’s add some content below the title!
  - Create a __`<h2>`__ header, which are just smaller `<h1>` headers --  __Step Nine for more info on headers__
2. We’ll give them a __class__ name using __class=”item”__ just before the closing of `<h2>` 
  - Feel free to name this whatever you want, but __“item”__ just makes sense for me + future-me
3. Let’s put the text down as __Dodge__ because that’s a future project you will build
  - There is no need for quotes around the words inside the tags

![](img/creating_project.gif)

## Part Five: Styling the h2 Tags/Items 

We can use a lot of the knowledge we’ve learned to finish this last part! Let’s tackle it with a list of things to do.
__Head to your main.css file:__

1. Let’s change the __text-color__ by using the __color property__ and a __value__ (i.e. #fff) 
2. Let’s change the __background-color__ by using the __background-color property__ and a __value__ (i.e. #000) 
3. Use __display: inline-block;__ to allow the items to be beside each other, but stack on top of one another for smaller screen sizes.
- We want to make a row of these “items” and continue to add to it as time goes on 
  - __display__ is a property that specifies how the area around the object is effected
  - __inline-block_ is a value that will allow us to put the objects beside each out, but when we get smaller displays (resizing the window), the objects will stack on-top of each other
    - An example of an __block element is a `<h1>`__ header
    - __Inline elements are beside each other__
4. Use __padding,__ which we discussed has background-color unlike margin, to create a button-look
- _Padding adds space inside the border of the text, but margin adds space outside of it
- We can use a shorthand instead of putting padding top, right, bottom and left
- __padding: 100px 150px 100px 150px;__ will __add padding clockwise__ → the 1st number is top, 2nd is right, 3rd is bottom, and 4th is left
- Even shorter is __padding: 100px 150px;__
  - The x and y axis will repeat -- __100px is the x axis__ and __150px is the y axis__

![](img/styling_items.gif)

## Part Six: Linking the Items

1. Let’s make it so that when you click one of our projects, it can link to a different page!
- __`<a href=“https://webpage.com”> </a>`__ tag __encloses other tags__ → linking to other webpages
- Between <a href=“https://webpage.com”> __and__ </a> you put your other element
2. Let’s enclose our item so it can link somewhere
- We are going to use an __hashtag (#)__ insert of an URL for now
  - This simply links to the same page we are on --  since we haven’t created these projects this is kind of like a __variable in math__
- `<a href=”#”>  <h1 class=”item”> Dodge </h2> </a>` 

![](img/linking_items.gif)

## Part Seven: The End

Congrats you’ve finished building the project section!

![Kanye saying yes](img/kanye_yes.gif)