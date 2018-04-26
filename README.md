# UsefulCSS

## Specialized Contextual Selectors & Pseudo Classes

Contextual Selectors select an element based on a sibling or ancestor which are known as descendant combinator selectors. 

An example is ```css section p ``` this selector affects all p tags that are descendants of section. 

### Specialized Contextual Tags
#### Child Selector (>)
```css tag1 > tag2 ``` In this example tag2 must be a child of tag1 or tag1 must be the parent of tag2. In the coding example attached we select all h2 elements in section and italicized them while also giving them a color of navy. 

#### Adjacent Sibling Selector (+)
```css tag1 + tag2``` In this example tag2 must immediately follow tag1. In the coding example you can see how the two paragraphs are differ from the use of this tag.

#### General Sibling Selector (~)
```css tag1 ~ tag2``` tag2 must follow (not immediately) its sibling tag1. In the example we see a p tags under h3 are affected. 

**Check this out** change the h3 tag to a h2 in the general sibling selector. Notice how the general sibling selector takes priority over the adjacent sibling selector.

#### The Universal Selector (*)
```tag1 * ``` The universal selector selects all elements within what you set tag1 to. In the code example all elements not assigned a color takes the value of blue.

#### General Selectors
This is a .classSelector and this is a #idSelector. 

When to use a class and when to use a Id? 
Use an Id to identify a unique element. An id should only be assigned to a element once! Use a class to identify a number of elements that will share the same characteristics.  

#### Attribute Selectors
Attribute selectors select elements based on the attributes of there HTML tags. It follows the syntax of tagName[attributeName] in the code you can see we use the alt tag. So the syntax looks like ```css div[alt]```

We can also target a element based on its attributeName value the syntax looks something like tagName[attributeName="attributeValue"] the example from our code is ```css div[alt="box2"]```



