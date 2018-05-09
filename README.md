# UsefulCSS

## Specialized Contextual Selectors & Pseudo Classes

Contextual Selectors select an element based on a sibling or ancestor which are known as descendant combinator selectors.

An example is `css section p` this selector affects all p tags that are descendants of section.

### Specialized Contextual Tags

#### Child Selector (>)

`css tag1 > tag2` In this example tag2 must be a child of tag1 or tag1 must be the parent of tag2. In the coding example attached we select all h2 elements in section and italicized them while also giving them a color of navy.

#### Adjacent Sibling Selector (+)

`css tag1 + tag2` In this example tag2 must immediately follow tag1. In the coding example you can see how the two paragraphs are differ from the use of this tag.

#### General Sibling Selector (~)

`css tag1 ~ tag2` tag2 must follow (not immediately) its sibling tag1. In the example we see a p tags under h3 are affected.

**Check this out** change the h3 tag to a h2 in the general sibling selector. Notice how the general sibling selector takes priority over the adjacent sibling selector.

#### The Universal Selector (\*)

`tag1 *` The universal selector selects all elements within what you set tag1 to. In the code example all elements not assigned a color takes the value of blue.

#### General Selectors

This is a .classSelector and this is a #idSelector.

When to use a class and when to use a Id?
Use an Id to identify a unique element. An id should only be assigned to a element once! Use a class to identify a number of elements that will share the same characteristics.

#### Attribute Selectors

Attribute selectors select elements based on the attributes of there HTML tags. It follows the syntax of tagName[attributeName] in the code you can see we use the alt tag. So the syntax looks like `css div[alt]`

We can also target a element based on its attributeName value the syntax looks something like tagName[attributeName="attributeValue"] the example from our code is `css div[alt="box2"]`

### Pseudo Classes

In the code there is a number of examples using pseduo classes. Psudeo classes can be grouped into two seperate categories.

**UI Pseudo Classes** Applies markup when a HTML element is in a certain slate.

**Structural Pseudo Classes** Rules are applied when structural relationships take place such as a element being first or last.

_Important Note_ A single colon(:) represents the use of a pseudo class. A double colon (::) represent pseudo classes that are new in CSS3.

The pseudo classes first used are ones that target anchor tags. The first instance is the `css a:link` selector, in the code this sets the color of all links to black. The next pseudo class used is the `css a:hover` check out what happens now when you hover over a link. The `css a:visited` is pretty straight forward, once a link is clicked the color then changed to orange.

The last pseudo class used is the `css a:target` when the user clicks a link that points somewhere else on that page that element is selected. Check out what happens when you click the writing at the top of the page. To set the syntax for a target class to work we first assign the href a #id like value. Next we assign the element we want to target and give it the same id as we did for the href(This is seen more clearly in the code).

## Floating and Clearing

Elements that follow a floated element will flow up beside them if there is room to do so.

The clear property is used to **stop** elements from flowing up beside floated elements.

We are going to look at three ways to deal with floating elements.

As you can see in _problem.html_ this is one of the problems that can arise when using floats.

#### Solution 1: Overflow hidden

Apply `css overflow:hidden` to the section tag as seen in _overflow.html_. What this does is create a block formatting context for the element. This is not the intended us of the `css overflow:hidden` as it is usually used to control what happens when content overflows it's parent container. But this is one way you can hack togehter floats to get the design you want.

#### Solution 2: Floating the parent

By floating the parent element to the left in this case the section tag the content becomes shrink wrapped. You can view this by removing `css width:100%` from the file _parentFloat.html_. Also try removing the `css clear:left` from the footer after and watch what happens. Since the section is now floated the footer will try to move up beside it. By giving the section a width of 100% it ensures the footer will sit directly below it. However do you see the problem the occurs when width is 100% but there is no clear applied to the footer? It takes on the height and width of the section. By adding a clear left we ensure that the element will sit directly below the section and no problems occur.

#### Solution 3: Adding a clearfix

One of the most common ways to clear floats is CSS today is using a clearfix.

## Menus

The first file _simpleMenu.html_ displays a simple vertical menu. By default li tags `display:block` so they will **stack vertically**. Another default to be aware of is that <a> tags are `display:inline` therefore shrink wrapping the content. By changing the display to block we are causing the <a> tag to extend and fill its whole parent making the whole area clickable not just the words themselves.

The last think I want you to look at is the use of the child selector. The cool thing about this slector here is we are applying styles to all the the <a> tags except the first.

**Horizontal Menu** To get the menu to display horizontally all we have to do is float the <li> elements to the left. We also float its parent element (<ul>) to make sure it encapsulates the <li> tags. To see this is action try removing `float:left` from ``list1 ul` and view the changes in the browser dev tools.

**Drop Down Menu**
The first thing to look at in _dropDown.html_ is the markup. We create the main nav items with a <ul>. From there with select the <li> tags we want a dropdown menu to come from. Within that <li> tag we create another unordered list.
