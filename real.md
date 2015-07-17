# TODO
- Errors (perhaps make it: "Did you run into this error? If so, click here")
- Break this tutorial down into multiple parts
    - Determining what's necesary
    - Figuring out your main thing
- Add instructions for what the students should actually do

# Budiling Instagram!

I have decided I want to build my own version of Instagram. This is literally how I did it.

# Part 1: Figuring Out If It's Possible

There are two core features of Instagram:

- taking photos
- adding filters on those photos

If I can't do that, then I can't build Instsagram. Therefore, I want to validate that I can even do that first. 

## 1. Can I Take Pictures?

I want my app to be able to take pictures on an actual phone. I have no idea how to do this so I Google.

### Googling For Taking Pictures

- `how do I take photos in my app`
    - problem: you are not building an app, you are building a website
- `how do I take photos on my website`
    - problem: you don't mention you're trying to use javascript
- `how do I take photos on my website javascript`
    - problem: the phrases `how do I` and `on my website` are extraneous, omit then and try
- `take photos javascript`
    
Ok, now we have some results:

![](https://s3.amazonaws.com/f.cl.ly/items/0E2n1f3t1V0L181t0l2O/Image%202015-07-16%20at%204.52.34%20PM.png)

- Normally, I usually open the first 3 links in new tabs but because I see `developer.mozilla.org` and I know that it is a legit, I open [the first link](https://developer.mozilla.org/en-US/docs/Web/Guide/API/Camera).

### Checking For Relevancy The Resource

#### Relevancy:
The first thing I want to make sure that this article is relevant to my problem:

I read the title:
> Introduction to the Camera API
 
^ Sounds promising... I continue reading...

![](https://s3.amazonaws.com/f.cl.ly/items/3d4010271F2g0A2b2p35/Image%202015-07-16%20at%204.43.17%20PM.png)

^ Cool! This tells me I can take pictures with my device's camera, exactly what I want!

#### Will Those Code Work?

The next thing I'll immediately look for is some type of working example. I want to make sure that if I follow all the stuff on the page, my code will be able to take a photo.

I scroll down to the bottom of the page and see:

![](http://f.cl.ly/items/441S3U2I3a1f3o2G1k1x/Image%202015-07-16%20at%204.46.21%20PM.png)

I open the link ([http://robnyman.github.com/camera-api/](http://robnyman.github.com/camera-api/)) on my phone and test to see if it works...

And YES, it does!

Great, now I've found code that I know that works and it is likely that if I follow the instructions, I'll be able to take a photo on my phone. Note that I still have NO idea how to use this code, but that's for me to figure out later.

## 2. Can I add filters?

For the photos that I take, I want to be able to add instagram like filters to it. I have no idea how to do this so I Google.

### Googling For Filters

- `how do I use instagram's filters on my website`
    - problem: missing javascript
- `how do I use instagram's filters on my website javascript`
    - problem: extraneous words
- `instagram filters javascript`
    - great.

![](https://s3.amazonaws.com/f.cl.ly/items/1X0U3b0Z051M3a333e3R/Image%202015-07-16%20at%206.09.05%20PM.png)

I decide to open all 3 links in new tabs:

![](https://s3.amazonaws.com/f.cl.ly/items/2C240b2d3Y0R381Y1t0d/Image%202015-07-16%20at%206.12.46%20PM.png)

#### From the [first google link](http://techslides.com/instagram-image-filters-with-html5-canvas):

##### Determining Relevancy
I read the first paragraph to find:

![](https://s3.amazonaws.com/f.cl.ly/items/392g3z2R2C1L3U1Z3z15/Image%202015-07-16%20at%206.13.53%20PM.png?t=1437095673260)

> There are many image processing libraries today that could be used to recreate Instagram photo effects in the browser

which confirms that this article is relevant to me.

##### Understanding

A bit lower in the article links to many different resources. I open each one in a new tab to explore it:

![](https://s3.amazonaws.com/f.cl.ly/items/1Y2I1L3U083a3S3B4604/Image%202015-07-16%20at%206.17.06%20PM.png)

I won't go into the details of the next part but from looking at each of these websites, it has made me confident that code exists that will allow me to add filters to my photos.

# Part 2: Scoping My Project

## Scoping Your Project

### Build the Scooter

Say you wanted to build a transportation vehicle that let you travel as quickly as possible across the US. Airplanes are fast—so perhaps building an airplne would be an ideal solution?

Well, building an airplane is really hard. I might first want to try my hand at building a car first. Well, even a car is too hard. Maybe I'd want to build a bike first. Well bikes still have all those complex gear things, maybe I'l build a scooter first.

Cool, I can figure out how to build a scooter. I'm not saying that I'm not going to build a bike. Once I've had practice my building skills by building a scooter, I then might try my hand at building a bike, and then a car, and then maybe even an airplane!

### Analyzing the Airplane

I still want to eventually build the airplane, so I'm going to design what I want my airplane to look like first before I decide to scope it down

So I decide to start looking at the instagram app:

When I open the app, I can see a feed of all my and my friends photos:
![](http://i.imgur.com/RIXijgF.jpg)

When I click the camera button, it opens the camera.

![](http://i.imgur.com/O2suv3m.jpg)

When I tap on the circular blue button, it takes a picture of me and presents a list of filter options I can filter my photo by.

![](http://i.imgur.com/QEmCs7L.jpg)

When I click on a filter, it applies that filter to my photo.
![](http://i.imgur.com/hkRzNwJ.jpg)

When I tap next, I see a screen that lets me share my photo.

![](http://i.imgur.com/WW4eTP5.jpg)

When I type in "Write a caption..." box, it lets me add a caption for my photo.

![](http://i.imgur.com/vfR2nhS.jpg)

When I tap Facebook, it enables the option that makes it so that when I tap "SHARE ->", it will post on my Facebook wall.

![](http://i.imgur.com/tkNaDsM.jpg)

So if I were to break down these components of the instagram app they are

- newsfeed
- camera button
- take picture button
- filters
- caption
- share to social media

### Deciding What The Scooter Is

So the most obvious features to remove are

- the newsfeed
- sharing on social media

Now we're left with

- camera button
- take picture button
- filters
- caption

Then you realize that you can actually remove

- filters
- caption

This leaves you with an app that lets you just take photos.

Now I challenged myself to make it even simpler:

Instead of trying to take an actual photo from the camera (which we saw above seemed quite challenging), what if we used an existing photo that was already on the internet instead?

What if the computer just asked you for a URL of a picture and then it just added it to a page?

We have our scooter. We'll call it "Add Image To Page"

# Part III: Building The Scooter: "Add Image To Page"

So my Scooter is building an app is more like a photo album for existing images that are on the internet.

I could try googling for `how do I build a photo album in javascript` which would probably give me pretty decent results, but because I know very specifically that I want to build the simplist photo album possible, this search may not do it for me.

## The Scooter Isn't That Easy
- front wheel
- back wheel
- handle
- steering shaft
- base
- etc.

I don't want to build the entire scooter all at once, I still want to break it down and build the front wheel first, then the back wheel, then maybe the handles, etc.

## Breaking Down The Components

We have to ask what the components are:

- when I click a button
- ask the user to give it a URL to an image
- add the image to the page

At this point, I could try googling `when I click a button add a photo to the screen`. This mentality will indicate that you're not breaking down the problem and trying to do it all at once.

Instead, it's easier for me to just figure out how to do something when a button is clicked. Anything! I don't care! I  can make it ask the user for a URL and then adding the image AFTER I figure out how to get the button working.

## Figuring Out How To Do Something When A Button Is Clicked

Here are a listing of Google queries sorted from the top down from worst to best.

- `know when the button is clicked and add an image`
    - Problem: You are coupling too problems, the button click, and adding the image. These are two problems! It will be easier to independently find and implement this.
- `know when the button is clicked`
    - Problem: You did not specifiy in what programming langauge
- `javascript know when the button is clicked`
    - Problem: The word "know" is unclear, what you really mean is "detect"
- `javascript detect when the button is clicked`
    - Problem: "The" and "is" is extraneous
- `javascript detect button click`
    - Great.

### Determining Which Resources Are Relevant

As always, I'll open the first 3 results in new tabs so I can have easy access to them:

[The first result](https://s3.amazonaws.com/f.cl.ly/items/3l0p170n3129232f2T45/Image%202015-07-16%20at%207.10.48%20PM.png) is a Stack Overflow page.

### Create A Base Project

- Getting off the ground
  - On the left file pane, right click and click `New Folder` to create a new
    folder. Name it `instagram`
- Make sure that live reload is running by opening a new terminal and typing `live_reload`
- Create a new file inside of instagram called `index.html` and double click
it to open it
  - Go ahead and type the following code into the open file (don't copy and
    paste it! and make sure to indent properly!).

    ```html
    <!DOCTYPE html>
    <html>
      <head>
      </head>
      <body>
      </body>
    </html>
    ```


### Understanding (this) Stack Overflow Page.
Stack overflow is a great Q&A resource that almost every programmer I know uses. There is a particularly good way to read Q&A type sites like Stack Overflow

#### Step 1: Read the Title

This step is done to determine relevancy.

So I read the title:

![](https://s3.amazonaws.com/f.cl.ly/items/0X1U2Q0o3Y3u1G3X2S0j/Image%202015-07-16%20at%207.13.54%20PM.png)

> How to check whether a Button is clicked by using JavaScript

^ This seems pretty relevant to me.

#### Step 2: Find The Best Answers

I skip the rest of the question because it already seems relevant. I then immediately jump to the answers section () that either has the most upvotes and / or has the green checkmark (the answer selected to be the best by the person who asked the question—we'll call this "asker's choice")

In this case:

![](https://s3.amazonaws.com/f.cl.ly/items/3p0j0q1H2f1w1T1Y2n20/Image%202015-07-16%20at%207.18.26%20PM.png)

- it has the most upvotes (16)
- and has the asker's choice

#### Step 3: Test the Answer

So instead of taking any code and applying it to my own code immediately, I usually test my code in an isolated environment (just the code by itself). I personally like using a site like [JSBin](http://jsbin.com)

In this case however, the answer provides [a working example already](http://jsfiddle.net/6qDap/1/):

![](https://s3.amazonaws.com/f.cl.ly/items/3E3b352W2Y2T0z1Z3z33/Image%202015-07-16%20at%207.21.49%20PM.png?t=1437099734735)

[This example](http://jsfiddle.net/6qDap/1/) is inside of a JS Fiddle (another sandbox / isolated environment like JS Bin).

And so I test it out by pressing the enter button and it indeed makes an alert every time I press enter!

Great! Now I have validated that I have found code that works in order to do something when a button is clicked (in this case it makes an alert when the button is clicked!)

![](https://s3.amazonaws.com/f.cl.ly/items/433h1I2f422T0l032v3a/Image%202015-07-16%20at%207.24.49%20PM.png)

![](https://s3.amazonaws.com/f.cl.ly/items/3U1Y2w0p0x3e0p0w3Z1V/Image%202015-07-16%20at%207.25.15%20PM.png)

Here is the code from the example:

```html
<!--HTML Code-->
<input id="button" type="submit" name="button" value="enter"/>
```

```js
// Javascript Code
var count = 1;
document.getElementById('button').onclick = function() {
   alert("button was clicked " + (count++) + " times");
};
```

[![](http://i.imgur.com/9KuKZGN.png)](http://jsfiddle.net/6qDap/1)

#### Step 4: Cleaning Up The Answer

It's easiest for me to understand something when I'm working with the bare bones.  I want to make sure that I understand the example, so I'll remove as many things as possible to allow it to still work.

This makes it seem like I can remove this stuff about count in the Javscript which leaves me with [this code](http://jsfiddle.net/6qDap/1609/)

```html
<!--HTML Code-->
<input id="button" type="submit" name="button" value="enter"/>
```

```js
// Javascript Code
document.getElementById('button').onclick = function() {
   alert("button was clicked");
};
```

It still works : ) 
[![](http://i.imgur.com/9KuKZGN.png)](http://jsfiddle.net/6qDap/1609/)

##### Step 5: Tinkering for Understanding

[Here's a video](https://www.youtube.com/watch?v=HlVbolRGz4o) I put together for how I play with things to learn what it does.

##### Step 6: Now I'll try to add it to my code:

Warning: BELOW CODE DOES NOT WORK

```html
<!--index.html-->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <script src="main.js"></script>
</head>
<body>
  <input id="button" type="submit" name="button" value="enter"/>  
</body>
</html>
```

```js
// main.js

document.getElementById('button').onclick = function() {
   alert("button was clicked");
};
```

##### Step 7: Debugging The Code

The first thing you should do when something doesn't work when you're working with HTML & Javascript is to open the developer console. This is because any errors that occur will be shown in the developer console and if there were to be any errors, they would completely disable any of the javascript from functioning properly.

![](https://s3.amazonaws.com/f.cl.ly/items/433z0g281v0V0E242j47/Image%202015-07-17%20at%204.22.28%20AM.png)

From the above, we can see we have the error:

> Uncaught TypeError: Cannot set property 'onclick' of null

If we want to know exactly where the errors is in the code we can click to the right of the error:

![](https://s3.amazonaws.com/f.cl.ly/items/3O2B37083s2f462v1Z0N/Image%202015-07-17%20at%204.24.40%20AM.png?t=1437132296160)

Which takes us to this screen:

![](https://s3.amazonaws.com/f.cl.ly/items/2d2F1V2D3S3t1d2X0I1q/Image%202015-07-17%20at%204.26.04%20AM.png)

Now, I'm still not sure what that means, so the first thing I do is Google it:

![](https://s3.amazonaws.com/f.cl.ly/items/231p3i1q271g1j2f2X0d/Image%202015-07-17%20at%204.27.45%20AM.png)

And I open the first 3 pages in new tabs:

Looking at the [first page](http://stackoverflow.com/questions/9778888/uncaught-typeerror-cannot-set-property-onclick-of-null)

- the title "Uncaught TypeError: Cannot set property 'onclick' of null" is relevant
- looking at the answers, this answer with 21 votes seems to be voted the highest and has the easiest to understand example:

![](https://s3.amazonaws.com/f.cl.ly/items/0A3Z3k2Z3x0M2r402x42/Image%202015-07-17%20at%204.28.59%20AM.png)

I think this means that I put my code where it says 
`// your code`
but I'm not sure so I'll keep looking

Looking at the [next google result](http://stackoverflow.com/questions/17080502/uncaught-typeerror-cannot-set-property-onclick-of-null), the title is still relevant and it seems to answer my question:

![](https://s3.amazonaws.com/f.cl.ly/items/0T003P1z1u2F041d0K3F/Image%202015-07-17%20at%204.31.43%20AM.png)

At this point I could try to isolate this code to test it out but it seems simple enough but more importantly, critical that my original code be in here, so I will just update the `main.js` file to this:

```js
// main.js

window.onload = function() {
  document.getElementById('button').onclick = function() {
     alert("button was clicked");
  };
};
```

and now it seems to work!

### Ask The User

So now we need to ask the user to give us a URL to an existing image. So to figure out how to do that, we could google the following (where the top is the worst and the bottom is the best)

- "ask me for a link of an existing photo"
- "ask user for link of existing photo"
- "ask user for text"
- "javascript ask user for text

Using the same Googling procedure above of opening the first 3 tabs, from w3 schools we see

![](https://s3.amazonaws.com/f.cl.ly/items/0J3T3j0I1V1E3i3N3h0k/Image%202015-07-17%20at%204.38.37%20AM.png)

I open the [Try it yourself](http://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_prompt)

which seems to work. And then try to simplify the example by removing everything below the line `if (person != null) {` and adding an alert.

[![](http://i.imgur.com/9KuKZGN.png)](http://jsbin.com/jawaga/1/edit?js,output)

#### Integrating the code:

```html
<!--index.html-->

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <script src="main.js"></script>
</head>
<body>
  <input id="button" type="submit" name="button" value="enter"/>  
</body>
</html>
```

```js
// main.js

document.getElementById('button').onclick = function() {
   var photoUrl = prompt("Give us a URL of a photo you want to add to the stream!")
   alert(photoUrl)
};
```
