# What is CSS ? Syntax and Way to apply

Css Means Cascading Style sheets. it is used to style Html, like colours, fonts, spacing and layout. it separates design from structure, so the same Html can look completely different with different Css.

Css - Cascading Style Sheet
Cascading- means rules flow down and later or more specific rules win.
Style - Appearence and Behaviour
Sheet - Our WebPages

## Types of CSS

### What are the three ways to add Css to page?

Inline Css is written directly in the style attribute of an element. Internal Css is written inside a style tag in the head. External CSS is Written in a separate css file and linked, which is the best practice because it is reusable.

There are Three Types of Css.

- Inline Css
- Internal Css
- External Css

## what is the difference between inline and external css perfomance wise ?

External css can be cached by the browser, so it loads faster on repeat visits and keeps the Html clean. Inline css is not cached and increases Html size, but it can be faster for a tiny amount of critical css above the fold. most projects use external css for everything.

### Inline Css

InLine Css in Our Inline Css we are write css Code in Our Html Elements. with style tag.

```
<p style="color:blue; background-color: red;"> This is Our Html Elements </p>
```

### Internal Css

Internal Css We are writing Css in our head tag with the help of Style Tag and we are using the selector tag for select our each element to styling.

```
<style>
p{
    color: red;
    background-color:blue;
}
</style>
```

### External Css

External Css In Our External Css we are making a new external file in our folder and link with html folder in our head tag. and write code in

```
<link rel="stylesheet" href="index.css">

```

### Selectors in Css

CSS selectors are patterns used to target and style specific HTML elements on a Web Page.

```
Selector{
    property: value;
}
```

We have Three Type of Selector.

### Element Selector

Element selector is for select the element

```
h1{
    color: blue
}
```

### Class Selector

Class Selector is for selecting a class element first we are create class in our element and then in css we are using . extension for select class element.
ex:

```
<h1 class="heading"> This is Class Element</h1>
style
.heading{
    color:blue;
}
style
```

##++# Id Selector
id Selector starts with # and selecting our Id Elements. we are using id Selector for our unique elements select.
x:

```
<h1 id="heading"> This is Class Element</h1>
style
#heading{
    color:blue;
}
style
```

### Universal Selector

Universal is for all this is use for all code selector we are using \* this is our universal selector.

```
*{
    In this Our all Elements
}
```

### What are CSS combinators ?

Combinators describe the relationship between selectors. A space select all descendants, the greater than sign selects direct children only, the plus sign selects the immediate next sibling, and the tilde selects all following siblings.

### Specificity

### what is Css Specificity ?

Specificity decides which css rule wins when two rules target the same element. inline styles are strongest, then ids, then classes, then element selectors. if specificity is equal, the rule written later wins.

which selector is more specificity
Inline css > id > class > element > \* Universal

### Pseudo Class

### What are pseudo Classes in Css ?

Pesudo classes style an element based on its state or position. common ones are hover, focus, active, first-child, last-child and nth-child. they are written with a single colon.

Element State Based Styling

Selector:pseudo class{
property: value
}

```
#h1:hover{
    background-color: red;
}
```

### Pseudo Element

### what is the difference between pseudo classes and pseudo elements ?

Pseudo classes target a state of an existing element, like hover, and use one colon. pseudo elements create a virtual part of an element, like before and after, and use two colons. Pseudo elements need a content property to appear.

Elements part state styling

```
h1::after{
    content: "Hii";
}
```
