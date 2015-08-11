# Box Model Dorm Posters Design

<img src="https://s3.amazonaws.com/after-school-assets/posters.jpg" alt="Posters" align="right" width="300" hspace="10">

You can tell a lot about a person by the posters they chose to buy and hang on their wall. I mean, that's commitment. You not only have to spend money, but you have to look at it every single day. 

This becomes really important as you start to select your roommate for college. You have to live with this person (and their posters) every day for a full year.

## Let's Get Started

### Step 1:

Take a Look at the `How To: Work On A Lab` to walk you through how to fork and clone this lesson.

### Step 2:

Open `index.html` in the browser by running in terminal `python -m SimpleHTTPServer 3000`. 

Once you have the server running, select `preview` and then `port 3000`.

<img src="https://s3.amazonaws.com/after-school-assets/nitrous-preview.png" alt="nitrous preview">

You'll notice so far, the site is just a blank canvas of categories for each type of poster. You're going to be responsible for arranging the posters nicely on the wall, and framing them (you're the one doing the judging so you decide what look's best).

You'll code your solution in `css/style.css`. Go ahead and open that file in Nitrous, as well as `index.html`.

### Step 3:

Let's take a look inside the `images` directory. You'll notice several posters: Audrey Hepburn, Michael Jordan, New York City, Picasso, Beyonce, Andy Warhol, Woody Allen, and the New York City skyline. The goal is to put each poster in their appropriate category and add a snazzy frame.


### Step 4: "The Classy Roommate"

If you look inside of `index.html`, you'll notice this image is already in the HTML, with the ID `audrey`. We can use this ID as our CSS selector.. 

<img id="audrey"  src="images/audrey.jpg" alt="Audrey Hepburn" align="right" width="100px" hspace="10">

First, we need to center the image. Copy and paste the following code inside of `css/style.css` right after the comment `/*"The Classy Roommate"*/`:

```css
#audrey {
  margin-left: auto;
  margin-right: auto;
  display: block;
}
```

Suddenly we're using a whole bunch of CSS properties we've never seen before!

`margin` is responsible for the space around the image we're styling. You can think of it as the space between pieces of content. In the case of the Audrey poster, we're talking about the space between the sides of the grey box and the poster. If we want the image to be centered, we want the same margin on the left and the right. `margin-left` and `margin-right` are two CSS properties that we set to `auto` meaning it will automatically center the image.

`display: block;` means that the image will take up the entire width of the grey box. Nothing can fill in next to it. Without the display block, we wouldn't have a margin to the left, because images by default will fill in next to each other.

And now to add the border:

```css
#audrey {
  margin-left: auto;
  margin-right: auto;
  display: block;
  /*Add this line to your CSS!*/
  border: 15px solid red;
}
```

`border: 15px solid red` means that our border around the image will be 15px wide, will be a solid line, and will be red in color.


### Step 5: "The Neurotic New Yorker"

<img src="images/woody.jpg" align="right" width="100px" hspace="10">
<img src="images/newyork.jpg" align="right" width="100px" hspace="10">


If we look at the page in browser in the developer tools, we can see that the Woody Allen poster is much smaller than the New York City poster. In fact, the Woody Allen poster is 171 x 253 pixels and the NYC poster is 236 x 364 pixels. If we want the frame to be the same size around both posters, we have to increase the size around the Woody Allen Poster.

We're using the ID `woody`, defined on the `img` tag in `index.html` to style the Woody Allen poster. Copy and paste the following code inside of `css/style.css` underneath the comment `/*"The Neurotic New Yorker"*/`:
```CSS
#woody {
  padding-top: 55.5px;
  padding-bottom: 55.5px;
  padding-left: 32.5px;
  padding-right: 32.5px;
  background-color: white; 
}
```

Next, we need to use padding to make this poster bigger. Padding is the space around the element, that goes inside the border. `padding-top` add space to the top, `padding-bottom` adds space to the bottom, `padding-left` to the left and `padding-right` to the right. If we want this image to be 236px wide, we need to add `32.5px` of padding to the right and the left. In order to make the image `364px` tall, we need to add `55.5px` of padding to the bottom and the top.

We also need to set the `background-color` to white so that the white fills in that padding.

And now we need to set the border - again `border: 15px solid red;`. You can change up the value of the border property to be smaller pixels in width, or dashed in style, or even purple in color!for the NYC poster, we add the following to `css/style.css`:

```css
#woody {
    border: 15px solid red;
    padding-top: 55.5px;
    padding-bottom: 55.5px;
    padding-left: 32.5px;
    padding-right: 32.5px;
    background-color: white; 
}
```

And now for the New York City poster, we just need to add a border. Copy and paste the following code inside of `css/style.css` underneath the CSS for the Woody Allen Poster:

```css
#newyork {
  border: 15px solid red;
}
```

### Step 6: "The Art History Major"

<img src="images/picasso.jpg" align="right" width="100px" hspace="10">
<img src="images/warhol.jpg" align="right" width="100px" hspace="10">

For this one, we need to resize the images so that they fit on the wall, and then frame them together in one big frame.

First, let's resize the image using the `height` css property. Copy and paste the following code inside nside of `css/style.css` underneath the `/*"The Art History Major"*/` comment:

```css
#warhol {
  height: 300px;
}

#picasso {
  height: 300px;
}
```

Now, our images are the same height and fit on the wall properly! Next up, we need to put a frame around both images. We can't just add a border to each poster, because that would frame them separately. If you look at `index.html`, you'll notice that both `img` tags are nested inside of a `div` with the class `double`.

That class is what we want to use as our CSS selector and apply styling (like the border to). Let's add this CSS to `css/style.css` too:

```css
.double {
  border: 20px solid navy;
  text-align: center;
  background-color: white; 
}
```

First we set a 20px wide, solid navy border around both images using the `border` property. 

But you'll notice that both images are still flushed to the left. We can use the `text-align` property and give it the value `center` to center the images. 

Finally, you'll notice the grey background is still visible between the posters. Lets set `background-color: white` to act as a matte behind the posters.

### Step 7: "Pop Culture Fanatic"

<img src="images/michael-jordan.jpg" align="right" width="100px" hspace="10">
<img src="images/beyonce.jpg" align="right" width="100px" hspace="10">

For these posters, we want to stack them on top of each other, center them, and add a unique border to each one.

First, we need to resize both images. Copy and paste the following code inside of `css/style.css` underneath the comment `
/*"Pop Culture Fanatic"*/`:

```css
#mj {
  height: 200px;
}

#beyonce {
  height: 300px;
}
```

Next, we need to center both images, but auto setting the `margin-left` and `margin-right`.

```css
#mj {
  height: 200px;
  margin-left: auto;
  margin-right: auto;
}

#beyonce {
  height: 300px;
   margin-left: auto;
  margin-right: auto;
}
```

Finally, we need to set the borders: 

```css
#mj {
  height: 200px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  border: 7px solid black;
}

#beyonce {
  height: 200px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  border: 10px solid purple;
}
```

## Tell Me More About The Code

Border, padding, and margin are all a part of the Box Model. The box model is a fundamental concept of CSS that determines a site layout and will dictate how the browser sizes our elements on the page. Every single HTML element (or piece of content) is viewed as a box with a width, height, padding (spacing inside), margin (spacing outside), and a border.


## How It Works


Take a look at the image below to get a sense of how these properties come to play. The blue background is considered the content that you're styling. 

+ `Margin` is the spacing between the element you're styling and other elements (top, right, bottom, and left)

+ `Border` is a decorative border around the element you're styling (top, right, bottom, and left)

+ `Padding` is spacing between the element itself and the border (top, right, bottom, and left)
 
<img src="https://s3.amazonaws.com/after-school-assets/box_model.png">

Take a look at [this code example](http://jsfiddle.net/flatiron_school/jtFgz/) to see how we can use the box model to size and separate two different divs on a page.

### Margin

Let's say I have two divs on a page, and I want to separate them by 50px. I would use the `margin` CSS property to separate them. In [this example](http://jsfiddle.net/flatiron_precollege/g2b6j6gh/2/) we have two divs, one orange and one blue. Each div has `margin: 50px;` set, which means there is 50px of space from the left, top, right, and bottom from any other element. There is no way to get another piece of content closer to either div on any side.

### Border

Let's take a div and add a 10px wide solid purple border. You can set each border property separately like in [this example](http://jsfiddle.net/flatiron_precollege/zpw244hj/).

```css
border-style: solid;
border-color: purple;
border-width: 10px;
```

You can also short-hand the whole thing:

```css
border: 10px solid purple;
```

### Padding

Now let's say I want to have some padding between the text and the border. The border surrounds the element, which in this case is the text `Flatiron //`, so we'd need to set some padding! In [this example](http://jsfiddle.net/flatiron_precollege/hwk5yz4t/), we set `margin: 20px;` which separates 20px from the top, right, left, and bottom of the div. 


### Additional Resources

1 [Mozilla Developer Network Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)

2 [W3C Schools Box Model](http://www.w3schools.com/css/css_boxmodel.asp)

3 [CSS Box Model Tricks](https://css-tricks.com/the-css-box-model/)




