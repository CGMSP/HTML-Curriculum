# Intro to HTML & CSS

## Table of Contents

* [Notes](#notes)


* [HTML](#html)
  * [DOCTYPE, HTML, Head, and Body](#doctype-html-head-and-body)
  * [Headings](#headings)
  * [Paragraphs](#paragraphs)
  * [Images and Attributes](#images-and-attributes)
  * [Lists](#lists)
  * [Links](#links)
  * [Divisions and Classes](#divisions-and-classes)


* [CSS](#css)
  * [Style](#style)
  * [Background](#background)
  * [Class Selector](#class-selector)
  * [More Styles](#more-styles)


* [Finishing Up](#finishing-up)
  * [Title](#title)
  * [Final Code](#final-code)


## Curriculum

### Notes

* First off, this is what we're making: [Click This](https://cgmsp.github.io/HTML-Curriculum/)


* Modern browsers are very forgiving on what is or isn't included in an HTML document. Browsers would rather guess what you meant than serve up an error or broken webpage. For that reason, most everything we mention is considered *best practices* meaning it's recommended but not required.

* It's also important to note that whitespace (spaces, tabs, blank lines) is generally ignored in HTML. It's good to indent your code so it's easy to read, but don't worry about getting it to look exactly like our code. We change the indents as needed to emphasis certain structures.

### HTML

##### DOCTYPE, HTML, Head, and Body

Pages tend to start off with four things: the `DOCTYPE` declaration, the `html` tag, the `head` tag, and the `body` tag.

The `DOCTYPE` tells the browsers how to display the page. There used to be several different `DOCTYPE`s, but as of the release of HTML5, you will almost certainly ever write `<!DOCTYPE html>`. This signals to the browser to render the page using HTML5 standards (the current HTML standard).

The `html` tag is the container for the `head` and `body` containers. It signals to the browser that everything between the tags are HTML. Note that while the `DOCTYPE` declaration didn't have a closing tag, that `html`, `head`, and `body` all have opening and closing tags so you can put stuff between them. Tags `<br>` (line break), and `<hr>` (make a big line on the webpage) also don't need a closing tad. This is because the line break or the line doesn't go on forever. However, text ends. This is why tags like `<p>` (paragraph) and headings need closing tags. The `<div>` tag is for dividing the page up, so they need closing tags.

`head` and `body` are the containers for the rest of the content. For information you want the user's browser to know or search engines to know, you use `head`. Content that you want displayed to the person visiting your site, you use `body`. Just remember, if the user is meant to see something it probably goes in the `body`, otherwise it should go in the `head`.

```HTML
<!-- index.html -->

<!DOCTYPE html>
<html>
  <head>

  </head>

  <body>

  </body>
</html>
```

#### Headings

If you were to look at a book, you would see that it's broken into several smaller parts and each part has a title. There's the book title, then the section titles, then the chapter titles, and then maybe chapter sub-sections:

* Main Title
  * Part 1
    * Chapter 1
    * Chapter 2
  * Part 2
    * Chapter 3
    * Chapter 4
      * Part 1
      * Part 2

In HTML we have headings too, in fact we have six: `h1`, `h2`, `h3`, `h4`, `h5`, `h6`. `h1` is your main heading and `h6` is the smallest heading. We're going to add headings to let people know what our site is called and what our sections are called.

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>


</body>

</html>

```

#### Paragraphs

The `p` tag is used very regularly and indicates to the browser that we're writing a *paragraph*. Just like most HTML tags, it has an opening tag and a closing tag with the content in the middle.


#### Images and Attributes

Now it's time to add an image using the `img` tag. `img` is one of those weird tags that doesn't use a closing tag, so you don't have to worry about that. What we will be adding though are __attributes__. Every HTML element can have attributes, and they just tell the browser how to handle the element. For instance `img` will need a `src` (source or location of the image) and `alt` (alternative text that describes the image if it doesn't load or if the user is unable to see the image).


```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>
<hr>
<p>This is an image of me!</p>
    <img src="https://avatars0.githubuserconte  nt.com/u/49257206?s=460&v=4" alt="Me!" />



</body>

</html>

```

#### Lists

HTML gives us two types of lists: unordered lists (`ul`) and ordered lists (`ol`).  The only difference between `ul` and `ol` is that `ul` uses bullet points and `ol` uses numbers. These two tags are containers for any number of list items (`li`) that you want included in your list. We need both for the recipe, `ul` for ingredients and `ol` for the directions:

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>
<hr>
<p>This is an image of me!</p>
    <img src="https://avatars0.githubuserconte  nt.com/u/49257206?s=460&v=4" alt="Me!" />


    <h3>About Me</h3>
      <ul>
        <li>I am this</li>
        <li>I am that</li>
        <li>I am good at this</li>
        <li>But not that</li>

      </ul>

</body>

</html>

```

#### Links

Now we want to have a list of links for our "Links" section. For links we use the `a` tag which requires a `href` attribute ("Hypertext Reference") to tell the browser where the link goes. In between the `a` opening and closing tag we add a description of the link. So here we just add links inside of our `li` tags to create a list of links:

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>
<hr>
<p>This is an image of me!</p>
    <img src="https://avatars0.githubuserconte  nt.com/u/49257206?s=460&v=4" alt="Me!" />


    <h3>About Me</h3>
      <ul>
        <li>I am this</li>
        <li>I am that</li>
        <li>I am good at this</li>
        <li>But not that</li>

      </ul>

      <h3>Contact Me</h3>
      <ul>
        <li><a href="https://www.github.com/kazmalhotra">GitHub: KazMalhotra</a></li>

        <li><a href="mailto:malhotrak@catlin.edu">Email: malhotrak@catlin.edu</a></li>

      </ul>


</body>

</html>

```

#### Divisions and Classes

The `div` tag is very important to designing a website even though it doesn't really DO anything. `div` stands for "division" and is just a way for us to group content together and divide it from other content. It's often assigned a *class* name that can be used by CSS to apply a certain type of decoration or *style*. This might seem a little confusing now, but should make sense when we get to CSS.

We'll make a `div` with the class name `font` that wraps around everything that specifies the font:

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
<div class="font">
  <head>
  </head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>
<hr>
<p>This is an image of me!</p>
    <img src="https://avatars0.githubusercontent.com/u/49257206?s=460&v=4" alt="Me!" />


    <h3>About Me</h3>
      <ul>
        <li>I am this</li>
        <li>I am that</li>
        <li>I am good at this</li>
        <li>But not that</li>

      </ul>

      <h3>Contact Me</h3>
      <ul>
        <li><a href="https://www.github.com/kazmalhotra">GitHub: KazMalhotra</a></li>

        <li><a href="mailto:malhotrak@catlin.edu">Email: malhotrak@catlin.edu</a></li>

      </ul>
</div>


<style>
.font{
  font-family: "Sans Serif";


}

</style>


</body>

</html>


```

### CSS

#### Style

Now for the `head`! We're going to write some rules that tell the browser how to format the page. We don't want the user to see the rules, just to see how the browser renders them; that's why we put it in the head. We'll be using CSS in the HTML file, and to do that we have to tell the browser to read it as CSS by using the `style` tag.

```HTML
<!-- index.html -->

<head>

  <style>

  </style>

</head>
```

#### Background

CSS is different from HTML and is written differently. With CSS you select what element or elements you want to change, what about them you want to change, and how to change that attribute. So if I want to change the background color for the `body` element, I write:

```CSS
body {
  background: wheat;
}
```

The brackets, colon, and semi-colon are all important and required.

#### Class Selector

Remember how we added a class to the `div`? Well that was so we could select that div with CSS. To select a class, you add a period before the class name:

```CSS
.container {
  background: white;
}
```

#### More Styles

There's no way we can go through all of the CSS rules (just like we can't go through all of the HTML tags); there are way too many of them. The best way to learn is to build! When you want to change something, look up what rule you should use. For this project, we'll use just a few more:


We set `margin` to zero so no space between our container `div` and `body` element will occur. Setting `width` to 100% tell the `img` to be as big as it can be, as long as it stays within the container `div`.

The container `div` has the most rules. `padding` is the space between the element border and content. We set this to 6 pixels so the words aren't right next to the border. `margin` is the space between the border and the element outside of the selected element. We set this to auto so the container will be centered. The `max-width` rule states "I don't care how small you get, but don't ever get wider than 600 pixels". Finally we add a `border` that is 4 pixels wide, solid, and seagreen in color.

This is our `head` so far:

```HTML
<!-- index.html -->
<style>
.font{
  font-family: "Sans Serif";
}

.centered{
  text-align: center

}

</style>
```

### Finishing Up

#### Title

We want the browser to know the name of our site. We use `h1` for the `body` and `title` for the `head`.

```HTML
<head>

    <title>Recipe Book</title>

    <style>
      body {
        background: wheat;
        margin: 0;
      }

      img {
        width: 100%;
      }

      .container {
        padding: 6px;
        margin: auto;
        background: white;
        max-width: 600px;
        border: 4px solid seagreen;
      }
    </style>

</head>
```

#### Final Code

That's it! A working website that you can add whatever you want to!

Here's the final code:

```HTML
<!-- index.html -->
<!DOCTYPE html>
<html>
<div class="font">
  <div class="centered">
  <head>
  </head>
<body>

  <h1 style="font-size:50px">My Website</h1>
  <p>By Me</p>
<hr>
<p>This is an image of me!</p>
    <img src="https://avatars0.githubusercontent.com/u/49257206?s=460&v=4" alt="Me!" />
</div>
<hr>

    <h3>About Me</h3>
      <ul>
        <li>I am this</li>
        <li>I am that</li>
        <li>I am good at this</li>
        <li>But not that</li>

      </ul>

      <h3>Contact Me</h3>
      <ul>
        <li><a href="https://www.github.com/kazmalhotra">GitHub: KazMalhotra</a></li>

        <li><a href="mailto:malhotrak@catlin.edu">Email: malhotrak@catlin.edu</a></li>

      </ul>
</div>
<hr>

<style>
.font{
  font-family: "Sans Serif";
}

.centered{
  text-align: center

}

</style>


</body>

</html>

```
