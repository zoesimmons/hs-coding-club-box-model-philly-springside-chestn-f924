# Box Model 

<img src="https://s3.amazonaws.com/after-school-assets/model-in-box.jpg" width="300" align="right" hspace="10">

The box model is a fundamental concept of CSS that determines a site layout and will dictate how the browser sizes our elements on the page. Every single HTML element (or piece of content) is viewed as a box with a width, height, padding (spacing inside), margin (spacing outside), and a border.


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
