# mlf-svg-icons
Graphics in SVG-format for use in web based programs. Developed especially for use in My Little Forum.

The set looks in it's first steps more or less similar to the set, that is used in the default theme of My Little Forum 2. A refinement to get an independent style is a task for the time, the set is complete.

## Inclusion of the images

As an example for the inclusion with CSS as background image let's look at a link with the background image in front of the link text.

~~~
<!-- the HTML source-->
<a class="reload" href="index.html">reload the page</a>

/* the corresponding CSS rules */
a.reload {
	padding-left: 1em;
	background-image: url(images/reload.svg);
	background-repeat: no-repeat;
	background-size: 1em 1em;
	background-position: 0 center;
}
~~~

A further example shows the inclusion of an icon image as a HTML element. The attributes `width` and `height` sets the default size of 24x24 pixels because the images in itself have the size of 128x128 pixels. The size set with the attributes will be overwritten with CSS to make the page responsive.

The CSS defines the rules in the mobile first style. Show the icon with a size of `1.25em` as the default for mobile devices and in wider screens a bit smaller to make it matching with a fictional running text. That's _the idea of **the example**_.

~~~
<!-- the HTML source-->
<img src="images/reload.svg" width="24" height="24" alt="reload the page">

/* the corresponding CSS rules */
img[src='images/reload.svg'] {
	width: 1.25em;
	height: 1.25em;
}

@media screen and (min-width: 44em) {
	img[src='images/reload.svg'] {
		width: 1.1em;
		height: 1.1em;
	}
}
~~~

