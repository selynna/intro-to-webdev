# Intro to Web Development Workshop

## HTML

HTML stands for "Hyper Text Markup Language" and is the "skeleton" of web
development. It contains all the content on your page - this includes things
like text, images, etc.

Typically, we start off with an `index.html` - this is
the base file for a lot of HTML websites.

## CSS

CSS stands for "Cascading Style Sheet" and holds all the styles for the
website. Do you want a line to be bolded? Do you want a line to be larger? Do
you want to scale a picture down? All of that can be done within CSS. 

We'll be using `style.css` with the `index.html`!

### So, how do we get started? 

In the files provided, we have an `index.html` and `style.css` created for you.
You'll be making your website with these files.

### `index.html`

In the index.html, there's already some prefilled code - this is the general
template that a lot of websites use.

#### `<head>`

<head></head> contains "header files", where you can link your stylesheets (so
the CSS files). We'll come back to this later!

#### `<body>`

`<body></body>` contains all of the content of the page. This is where you put
images, text, etc. 

Let's start by adding some text! 

#### `<hx>`, `<p>`

For text, we have quite a few ways to put text on the page. We'll be going over
two in particular: header tags and paragraph tags. 

Header tags are usually denoted by `<h1>`, `<h2>`, ... `<hx>`. It usually will
make the text size a little bit bigger/bolded. 

Paragraph tags are usually denoted by `<p>`, and it'll put text on the page. 

We can add this into the HTML like so:

```
<!DOCTYPE html>
<html>
   <head>
   </head>

   <body>
      <h1>Hello!</h1>
      <p>I'm at Local Hack Day</p>
   </body>
</html>
```

#### Images

Want to add an image onto your page? We have an `<img>` tag for you to use!
We'll need to have a link to the image, though. Let's say we wanted to add an
ugly mustang:
http://media.gettyimages.com/photos/low-angle-view-of-a-horse-with-its-mouth-open-picture-id74424564

We can put this into an image tag like so: 

```
<img
src="http://media.gettyimages.com/photos/low-angle-view-of-a-horse-with-its-mouth-open-picture-id74424564">
```

If we add that into our HTML, it should look like this.
```
<!DOCTYPE html>
<html>
   <head>
   </head>

   <body>
      <img
      src="http://media.gettyimages.com/photos/low-angle-view-of-a-horse-with-its-mouth-open-picture-id74424564">
      <h1>Hello!</h1>
      <p>I'm at Local Hack Day</p>
   </body>
</html>
```

### Styling the HTML

Whoa, you might've noticed that the image is HUGE. How can we fix this? 

That's right, with CSS, which again, contains all the styling for the content.

#### Linking the CSS to the HTML

CSS is not standalone - you need to tell the HTML that you want to grab the
files from a specific stylesheet. 

We need to link it in the HTML in the `<head>`:

```
<link rel="stylesheet" type="text/css" href="style.css">
```

Our code should now look like this:

```
<!DOCTYPE html>
<html>
   <head>
      <link rel="stylesheet" type="text/css" href="style.css">
   </head>

   <body>
      <img
      src="http://media.gettyimages.com/photos/low-angle-view-of-a-horse-with-its-mouth-open-picture-id74424564">
      <h1>Hello!</h1>
      <p>I'm at Local Hack Day</p>
   </body>
</html>
```

#### Misc styling

So the image is really big - let's try changing the image width in the CSS.
Every time we want to alter something with the CSS, it'll look something like
this:

```
[tag] {
   size: [x]px;
}
```

For our image, you can do it like this:

```
img {
   height: 100px;
}
```

If you refresh the page, it should be a lot smaller than before. 

#### What else can we do? 

We can move everything into the center!  Let's say we wanted to put everything
on the page in the center. We can do this using text-align. Since everything is
in the body tag, we can wrap everything with the body tag like so:

```
body {
   text-align: center;
}
```

#### divs and classes

We can use "divs" to group everything together, and classes to target a
specific portion of the code. Check out the demo on the projector!

```
<div>
   <p>Hello!</p>
   <p>Hello 2</p>
</div>
```

```
<p class="hello">Hello</p>

.hello {
   font-size: 10px;
}
```

#### font-size, font-family, and font-weight

We can alter the font size, font weight, and the font itself! font-size is literally the
font size, and font-weight is the boldness/lack of boldness. font-family is the
actual font (so think Arial, Times New Roman, etc).

For example, `font-weight: bold` = bold, and `font-size: 36px` = a font size of
36px...which is bigger than normal. `font-family: Helvetica` will change the
font to Helvetica instead of the default Times New Roman.

#### background-color and color

We can also alter the background color of the page and the color of the text.

For example, `background-color: blue` will make the background blue, whereas
`color: blue` will make the text blue.
