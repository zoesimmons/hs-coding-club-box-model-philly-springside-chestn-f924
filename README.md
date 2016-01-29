# Box Model Dorm Posters Design

<img src="https://s3.amazonaws.com/after-school-assets/posters.jpg" alt="Posters" align="right" width="300" hspace="10">

You can tell a lot about a person by the posters they choose to buy and hang on their wall. I mean, that's commitment. You not only have to spend money, but you have to look at it every single day. 

This becomes really important as you start to select your roommate for college. You have to live with this person (and their posters) every day for a full year.

## Let's Get Started

### Step 1:

Click `Open` at the top of this page to bring this lesson down to Nitrous so you can edit files in the text editor.

<img src="https://s3.amazonaws.com/after-school-assets/new-open-in-nitrous.png">

### Step 2:

Open `index.html` in the browser by running in terminal `python -m SimpleHTTPServer 3000`. 

Once you have the server running, select `preview` and then `port 3000`.

<img src="https://s3.amazonaws.com/after-school-assets/nitrous-preview.png" alt="nitrous preview">

You'll notice so far, the site is just a mess of images on a grey and white screen. You're going to be responsible for arranging the posters nicely on the wall and framing them (you're the one doing the judging so you decide what looks best).

You'll code your solution in `css/style.css`. Go ahead and open that file in the Nitrous text editor, as well as `index.html`.

### Step 3:

Let's take a look inside the `images` directory. You'll notice several posters: Audrey Hepburn, Michael Jordan, New York City, Picasso, Beyoncé, Andy Warhol, Woody Allen, and the New York City skyline. The goal is to put each poster in their appropriate category and add a snazzy frame.


### Step 4: "The Classy Roommate"

<img id="audrey"  src="https://s3.amazonaws.com/after-school-assets/audrey-poster.jpg" alt="Audrey Hepburn" align="right" width="100px" hspace="10">

If you look inside of `index.html`, you'll notice this image is already in the HTML, with the ID `audrey`. We can use this ID as our CSS selector. 

First, we need to center the image. Copy the following code and paste it inside of `css/style.css` right after the comment `/*"The Classy Roommate"*/`:

```css
#audrey {
  margin-left: auto;
  margin-right: auto;
  display: block;
}
```

Suddenly we're using a whole bunch of CSS properties we've never seen before!

`margin` is responsible for the space around the image we're styling. You can think of it as the space between pieces of content. In the case of the Audrey poster, we're talking about the space between the sides of the grey box and the poster. If we want the image to be centered, we want the same margin on the left and the right. `margin-left` and `margin-right` are two CSS properties that we set to `auto` meaning it will automatically center the image.

`display: block;` means that the image will take up the entire width of the grey box. Nothing can fill in next to it. Without the `display: block;`, we wouldn't have a margin to the left, because by default, images will fill in next to each other.

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

<img src="https://s3.amazonaws.com/after-school-assets/woody-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/newyork-poster.jpg" align="right" width="100px" hspace="10">

For these two posters, we want to frame them individually, but have the frames be the same size. If we look at the page in the browser in the developer tools, we can see that the Woody Allen poster is much smaller than the New York City poster. You can look at the image size by just hovering your mouse over the image text like this:

<img src="https://s3.amazonaws.com/after-school-assets/image-size-inspect-element.png">

In fact, the Woody Allen poster is 171 x 253 pixels and the NYC poster is 236 x 364 pixels. If we want the frame to be the same size around both posters, we have to increase the size around the Woody Allen Poster.

We're using the ID `woody`, defined on the `img` tag in `index.html` to style the Woody Allen poster. Copy and paste the following code inside of `css/style.css` underneath the comment `/*"The Neurotic New Yorker"*/`:

```css
#woody {
  padding-top: 55.5px;
  padding-bottom: 55.5px;
  padding-left: 32.5px;
  padding-right: 32.5px;
  background-color: white; 
}
```

Next, we need to use padding to make this poster bigger. `padding` is the space around the element, that goes inside the border. `padding-top` adds space to the top, `padding-bottom` adds space to the bottom, `padding-left` to the left, and `padding-right` to the right. If we want this image to be 236px wide, we need to add `32.5px` of padding to the right and the left. In order to make the image `364px` tall, we need to add `55.5px` of padding to the bottom and the top.

We also need to set the `background-color` to white so that the white fills in that padding.

And now we need to set the border - again `border: 15px solid red;`. You can change up the value of the border property to be smaller pixels in width, or dashed in style, or even purple in color! Copy and paste the border below in `css/style.css`:


```css
#woody {
    padding-top: 55.5px;
    padding-bottom: 55.5px;
    padding-left: 32.5px;
    padding-right: 32.5px;
    background-color: white; 
    <!-- Add this to your CSS! -->
    border: 15px solid red;
}
```

And now for the New York City poster, we just need to add a border. Copy and paste the following code inside of `css/style.css` underneath the CSS for the Woody Allen Poster:

```css
#newyork {
  border: 15px solid red;
}
```

### Step 6: "The Art History Major"

<img src="https://s3.amazonaws.com/after-school-assets/picasso-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/warhol-poster.jpg" align="right" width="100px" hspace="10">

For this one, we need to resize the images so that they fit on the wall, and then frame them together in one big frame.

First, let's resize the images using the `height` css property. Copy and paste the following code inside nside of `css/style.css` underneath the `/*"The Art History Major"*/` comment:

```css
#warhol {
  height: 300px;
}

#picasso {
  height: 300px;
}
```

Now, our images are the same height and fit on the wall properly! Next up, we need to put a frame around both images. We can't just add a border to each poster, because that would frame them separately. If you look at `index.html`, you'll notice that both `img` tags are nested inside of a `div` with the class `double`.

That class is what we want to use as our CSS selector and apply styling (like the border) to. Let's add this CSS to css/style.css too

```css
.double {
  border: 20px solid navy;
  text-align: center;
  background-color: white; 
}
```

First we set a 20px wide, solid navy border around both images using the `border` property. 


The `text-align:center;` will center our image. Without that line of CSS, both images would be flushed all the way to the left side of the grey box.

The `background-color: white;` acts as a matte behind the posters. Without it, we would see the grey between the images and the border.

### Step 7: "Pop Culture Fanatic"

<img src="https://s3.amazonaws.com/after-school-assets/michael-jordan-poster.jpg" align="right" width="100px" hspace="10">
<img src="https://s3.amazonaws.com/after-school-assets/beyonce-poster.jpg" align="right" width="100px" hspace="10">

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
  <!-- Add this to your CSS -->
  margin-left: auto;
  margin-right: auto;
}

#beyonce {
  height: 300px;
  <!-- Add this to your CSS -->
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
  <!-- Add this to your CSS -->
  border: 7px solid black;
}

#beyonce {
  height: 200px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  <!-- Add this to your CSS -->
  border: 10px solid purple;
}
```

## Tell Me More About The Code

Border, padding, and margin are all a part of the Box Model. The Box Model is a fundamental concept of CSS that determines a site layout and will dictate how the browser sizes our elements on the page. Every single HTML element (or piece of content) is viewed as a box with a width, height, padding (spacing inside), margin (spacing outside), and a border.


## How It Works


Take a look at the image below to get a sense of how these properties come to play. The blue background is considered the content that you're styling. 

+ `Margin` is the spacing between the element you're styling and other elements (top, right, bottom, and left)

+ `Border` is a decorative border around the element you're styling (top, right, bottom, and left)

+ `Padding` is spacing between the element itself and the border (top, right, bottom, and left)
 
<img src="https://s3.amazonaws.com/after-school-assets/box_model.png">

Take a look at [this code example](http://jsfiddle.net/flatiron_school/jtFgz/) to see how we can use the box model to size and separate two different divs on a page. You'll notice in this example, two aqua boxes. The HTML is written in the top left corner, the CSS in the top right corner, and the output of both HTML and CSS in the bottom right corner. 

See if you can modify the two boxes. Using the classes defined on the two divs, see if you can change the borders. What happens if you make the padding 50px on the bottom box? What about adding a margin of 20px to the top box?

You can run your changes by pressing the button `Run` in the top left corner:

<img src="https://s3.amazonaws.com/after-school-assets/jsfiddle-run.png">

### Margin

Let's say I have two divs on a page, and I want to separate them by 520px. I would use the `margin` CSS property to separate them. In [this example](http://jsfiddle.net/flatiron_precollege/g2b6j6gh/2/) we have two divs, one orange and one blue. Each div has `margin: 50px;` set, which means there is 50px of space from the left, top, right, and bottom from any other element. There is no way to get another piece of content closer to either div on any side.

### Border

Let's take a div and add a 10px wide solid purple border. You can set each border property separately like in [this example](http://jsfiddle.net/flatiron_precollege/zpw244hj/).

```css
border-style: solid;
border-color: purple;
border-width: 10px;
```

You can also short-hand the whole thing. The order here is important. The `border-width` goes first, followed by `border-style`, and the `border-color`

```css
border: 10px solid purple;
```

### Padding

Let's take [this code](http://jsfiddle.net/flatiron_precollege/hwk5yz4t/). I want to have some padding between the text and the border. The border surrounds the element, which in this case is the text `Flatiron //`, so we'd need to set some padding! In this example, we set `margin: 20px;` which separates 20px from the top, right, left, and bottom of the div. 

### Mark As Done

Last step, as always, is to mark this lesson as done on Learn and backup your work on Github. In Nitrous, in the terminal in this lesson directory, enter `learn submit`.

### Share Share Share!

We love it when you show us your work! Screenshot the posters or your code and share with **\#flatironcodeclub** and **\#dormposters**


### Additional Resources

1 [Mozilla Developer Network Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)

2 [W3C Schools Box Model](http://www.w3schools.com/css/css_boxmodel.asp)

3 [CSS Box Model Tricks](https://css-tricks.com/the-css-box-model/)





<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-coding-club-box-model' title='Box Model Dorm Posters Design'>Box Model Dorm Posters Design</a> on Learn.co and start learning to code for free.</p>
