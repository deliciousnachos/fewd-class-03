# CSS Basics

## Learning Objectives

 - Predict image paths and apply relative paths to `<img>` and `<a>` tags.
 - Describe the DOM and draw simple DOM tree.
 - Apply and explain CSS specificity, importance, cascade and inheritance.
 

## HTML Markup Review

Go to your Explorer/Finder and go to today's class (03_css_basics). Inside you should find a folder that says "sample\_portfolio\_starter\_code". Drag the "sample\_portfolio\_starter\_code" folder onto the Sublime logo and it should open up.

Right now this file doesn't have any HTML markup in it. Let's apply some tags together.

## Linking With Paths

So far we've linked CSS files to our HTML files, but there are so many other things that we can connect while using paths. What else can you think of that we can link to?

**Linking To Websites**

The thing that probably pops into your head first when you hear the term "linking" is linking to another website. That's fairly simple to do with HTML while using the anchor or `<a>` tag.

**Syntax**: `<a href=""></a>`

**Linking To An Image**

By using the `<img>` tag, we can make images appear in the browser. Don't forget the alt attribute

**Syntax**: `<img alt="" src="">`

**To Another HTML file**

The same way that we can link to another CSS file, we can also link to another HTML file. This is similar to how websites link to other pages on the same domain. (i.e. from one Wikipedia article to another).  

**Syntax**: `<a href=""></a>`

**Group Practice**

Let's implement what we just learned. Right now we have our index.html file from our Sample Portfolio Starter Code folder. It has markup but not much else. In groups:

1. In the index.html file, where it says "About Me | Portfolio", make the word portfolio a link to portfolio.html
2. Similarly, in the portfolio.html file, where it says "About Me | Portfolio", make the word index a link to index.html
3. In portfolio.html, link the corresponding images for each project. The comments in the file also tell you what goes where
4. In index.html, where it says the name of different social media sites, link each name to the site it represents. For example, make the word "Facebook" a link to Facebook

**Recap**

- `<link>` are used to link to CSS stylesheets
- `<a>` tags are used to link to websites or other HTML files
- `<img>` tags are used to link to images. Note, that for `<img>` tags, the path goes in the "src" attribute, **not** "href"


## Back to CSS

![Peter Griffin CSS](./images/peter_griffin_css.gif)

**The DOM**

The **DOM** stands for *Document Object Model*. It's a visual representation of the HTML elements on a page.

![From University of Washington Computer Science & Engineering](https://courses.cs.washington.edu/courses/cse190m/10su/lectures/slides/images/dom_tree.gif)

One thing that you may notice is that the DOM is arranged sort of like a family tree. Actually, developers use the same terms that one would refer to in a family to describe the relationship between HTML elements.

For example, in the diagram above the `<h1>` and `<ul>` would be considered "siblings". Also, the `a` would be considered a "child" of the `<p>`.


### CSS and Specificity

Let's switch gears for a moment to CSS. Last class, we were styling many different elements on a page. So far, we've only been able to select elements by choosing *all* the instances of a certain element. But, we can get more specific then that by using other CSS selectors.

**CSS Selectors**

Element type selector

Ex: `p`

Descendant selector

Ex: `header h1`

Child selector

Ex: `header > h1`

Multiple selector

Ex: `p, a`

W3Schools has a [list of different CSS selectors](https://www.w3schools.com/cssref/css_selectors.asp) and let's you play around with them to see how they work.

They also have something called the [CSS Selector Tester](https://www.w3schools.com/cssref/trysel.asp) which lets you click on a selector to see exactly what elements would get targeted on the page.

### CSS and Importance

This is really helpful but it poses a question. What happens if an element is styled through an element type selector but also through another selector like the descendant selector. How does your CSS know how to decide what styling to apply? It decides through a concept called *inheritance*.

Importance in CSS means that one style will override another. Everytime you initially write a style in CSS you're overriding the default styles because anything that you type out is considered more important than it.

Element type selectors < Default styling

All other selectors < Element selectors

The key thing to remember is that the more specific the selector, the more important that it is. And the more important, the higher chance of having your style applied.

**Group Practice**

Try using the new selectors that you've just learned to style the index.html file. Remember to make your "styles" folder and to put a `style.css` file inside of it. Test out what happens when styles conflict and see which lines of CSS run.

### CSS and the Cascade

There is another situation where you have to deal with importance in CSS. Remember CSS stands for *Cascading* Style Sheets. This means that in CSS, styles are read from top to bottom. The effect that this has, is that the bottom-most styling is considered to be more important.

This can cause some confusion. How can you be sure of how your styles will come out when you have to deal with the cascade *and* different element selectors?!

**Tips**:

- **ALWAYS** style your HTML in the order that the elements appear in the file
- Try to be as specific as possible when targeting elements. I usually use the descendant selector with two or three elements.

**Note**: Everyone has different strategies for CSS but these have helped me out a lot. Remember, CSS is pretty weird. Peter Griffin understands the struggle of using it.

### CSS and Inheritance

It can be tiresome to have to write out so many styles for different HTML elements. You can repeat styles with the multiple selector, but even that could be troublesome to have to list out all the elements that you want to have a particular style. 

Thankfully, there is a certain aspect of CSS that can help with that.

Remember the family tree analogy I used earlier? The same way that people inherit traits from their family members, HTML elements can inherit traits from their family members!

Ex: If a font-size is applied to a ul, the li within them will get the same styling.

This can really help with writing faster, more efficient CSS. If you need a certain style to affect a large group of elements, see if it would make sense to give that style to the parent.

**Note**: Not all styling can be inherited. You *can* look up which styles won't work but most of them will. With trial-and-error, you'll run into the ones that don't.

## File Organization

If you haven't so already I want you to follow this format for your file structure. 

1. Create a FEWD folder on your Desktop if you haven't already
2. In it create a Homework folder
3. The homework folder should have folders for each week of the class, e.g. "Week 1, Week 2, etc"
4. When doing homework, put your repository into the corresponding week inside the Homework folder. For example, this week's homework would go inside "Desktop/FEWD/homework/week 1"

## Bonus

- Look up different CSS selectors and experiment with them
- Do you know what the Box Model is? If not, do some research and see if you can wrap your head around it
- Sublime has a lot of great shortcuts to make your life easier. There is a package called Sublime Tutor that walks you through a tutorial of a lot of tricks for it. Here are the instructions to get Sublime Tutor:
    1. Press `Ctrl+Shift+P` to bring command palette in front
    2. Type `Install Package` and press `Enter`
    3. Search for Sublime Tutor and press `Enter` to install the package




