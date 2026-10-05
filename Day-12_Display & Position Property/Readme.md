## **Lecture 12 CSS Display and Position property and Units**

- block
- inline
- inline-block
- none
- static
- relative
- absolute
- fixed
- sticky
- z-index

## **Display**

## Block Elements

### 1.What is a Block Element?

Ans: A Block-level element normally:

- Starts on a New Line
- Takes up the available width by default
- Allow width and height
- Allow margin and padding on all sides
- Stacks vertically with other block elements

Some Blocks Elements:

- Footer
- Nav
- main
- ul
- ol
- li
- form

```
<div> First Box </div>
<div> Second Box </div>

┌──────────────────────────────┐
│ First Box                    │
└──────────────────────────────┘
┌──────────────────────────────┐
│ Second Box                   │
└──────────────────────────────┘
```

## Inline Elements

### 2.What is an Inline Elements?

Ans: An Inline element normally:

- Does not start on a new line
- Takes only the space required by its content
- flows alongside other inline content width and height generally do not apply in the same way they do to block-level boxes
- Horizontal padding and margin work, while vertical spacing has different layout behavior and should be handled carefully.

Some Inline Elements:

- span
- a
- strong
- em
- label

```
<span> Hello </span>
<span> World</span>
```

## Inline-block Elements

### 3. What is inline-block elements?

The display: inline-block property combines the features of both An element with display: inline-block will appear on the same line as other inline or inline-block elements. In addition, you can set the width, height, margin-top, and margin-bottom properties for the element (like block elements).

Inline-block CSS is a CSS display Value

It Alow an Element to:

- In Same line with other elements

```

```

## Position in CSS

CSS has different positions that can be applied to elements. They include static, relative, absolute, fixed, and sticky. These positions specify how an element should be positioned in a document which causes the element to behave differently.

## Positioned and Non-positioned elements

Before looking at these position styles, the first thing to understand is positioned and non-positioned elements.

Non-positioned elements appear on a page following the order they are declared in the DOM, and they occupy as much space as they need. vertical and horizontal positioning ( top, left, right, bottom) cannot be applied to such elements because they are not positioned.

In contrast, vertical and horizontal positioning can be applied to positoned elements. positioned elements, by default, appear on a page like they are static, but using vertical and horizontal positioning can affect them differently, depending on the type of position.

- Static ( By default )
- Relative
- Absolute
- Fixed
- Sticky

---

**Static Posotion**
Static position is the default position style for elements. with this style, elements are non-positioned-- they appear as they are in the markup document. This style is also the only non-positioned style.

top, left, right, and bottom does not work with this style. You can visualize it with this code:

```
<div class="container">
  <div class="red-block"></div>
  <div class="blue-block"></div>
  <div class="green-block"></div>
</div>

.container {
  margin: 20px;
  height: 200px;
  display: flex;
  border: 1px solid black;
  padding: 20px;
  width: 400px;
}

.red-block,
.blue-block,
.green-block {
  width: 100px;
  height: 100px;
  margin-right: 20px;
}

.red-block {
  background-color: red;
}

.blue-block {
  background-color: blue;
  left: 20px;
  top: 20px;
}

.green-block {
  background-color: green;
}
```

The left and bottom style declarations on the blue block are ignored. Of course, you can apply margins, but that would affect the element after it:

```
.blue-block {
  /* ... */
  margin-left: 20px;
  margin-top: 20px;
}
```

---

**Relative position**
You can think of the relative position as a style that gives static elements more flexibility. But unlike static, elements with the relative position are considered positioned elements. This means that such elements can appear differently from the markup flow.

With relative, the element retains its flow in the document and occupies as much space as needed by default, but you can use positioning properties like top. The idea here is that the element is relative to its default position. Using these positioning elements moves the element around the default position without affecting others. Here is what I mean:

```
.blue-block {
position: relative;
top: 20px;
left: 50px;
}
```

Relative element in container

The blue block is still assumed to be filling up its default space, but positioning styles can move it around without pushing the others.

**Absolute position**
Elements with the absolute position are positioned elements that are removed from the flow of the document--like they are not there. Their space on the screen is taken away from them and assigned to other elements. Here's what I mean:

```
.blue-block {
/\* \*/
position: absolute;
top: 40px;
left: 50px;
}
```

**Absolute element in container**

As you would notice, the blue block's space earlier is now occupied by the green block. Even if you use margins on the absolute block, it does not affect the others. You can see it as the absolute element in its own territory outside the container.

As it is currently, the absolute element has no relationship with the container. Absolute elements are positioned within the closest relative positioned parent, and if none, they are placed within the viewport (browser window). For example, with a positioning style of left: 0, the element moves to the left edge of the relative parent or the viewport.

To set a relationship between the blue block and the container, you need to apply a relative class to the container:

```
.container {
/\* \*/
position: relative;
}
```

Now, you can push the blue block to the edges of the container:

```
.blue-block {
/\* \*/
bottom: 0;
right: 20px;
}
```

Absolute element with relative container

As you can see, the container serves as a boundary that the positioning properties can move the absolute element along. If there were no closest relative parents, the blue block would appear like this:

Absolute element without relative container

**Fixed position**
The fixed position is similar to the absolute position. The difference is that the fixed position does not respect any relative parents (or ancestors). It only respects the viewport. So a style like this:

```
.container {
/\* \*/
position: relative;
}

.blue-block {
/\* \*/
position: fixed;
top: 0;
left: 0;
}
```

will produce this:

Fixed element in viewport

The fixed element only respects the viewport regardless of the relative parent.

**Sticky position**
As the name implies, this makes an element stick to a container. The sticky position toggles between the relative and fixed position in a scrolling container. An element of this position style starts with the relative position, retaining its flow in the document. Upon scrolling in the container, if the specified positioning distance (with top, for example) is met, the element becomes fixed until the scrolling container is out of view.

Here's an example to explain this:

```
<div class="container">
  <div class="red-block"></div>
  <div class="blue-block"></div>
  <div class="green-block"></div>
  <div class="other-block"></div>
</div>
.container {
  width: 400px;
  height: 200px;
  border: 1px solid black;
  overflow-y: auto;
  margin: 20px;
  padding: 20px;
}

.red-block,
.blue-block,
.green-block {
width: 100px;
height: 100px;
margin-right: 20px;
}

.red-block {
background-color: red;
}

.blue-block {
background-color: blue;
position: sticky;
top: 10px;
}

.green-block {
background-color: green;
}

.other-block {
height: 500px;
margin-top: 20px;
width: 100%;
background-color: rgb(61, 61, 61);
}
```

At the start, the blue block appears in the flow of the document like this:

Sticky element before meeting condition

When you scroll in the container, and the blue block meets the top: 10px condition, it becomes fixed as you scroll:

Sticky element after meeting condition

You can try it on this codepen. Try scrolling in the container and see the blue block fixed.

Wrap up

In CSS, you have positioned and non-positioned elements. Non-positioned elements appear as the flow is declared in the markup. This applies to the static position style. Positioned elements may appear in the same flow in some cases (sticky and relative) and may not in some other cases (absolute, fixed), but they can be controlled with positioning styles (top, left, right, bottom).

In summary:

- static: default position style appears as the declared flow in the markup
- relative: appears as the declared flow but can be repositioned with respect to the default position
- absolute: leaves the flow, and another element occupies the default position. It can be repositioned with respect to the closest relative element if available; else, the viewport
- fixed: leaves the flow and can be repositioned with respect to the viewport
- sticky: behaves as relative, and when a specified positioning distance condition is met in a scrolling container, it becomes fixed.

## Z-Index

**_4.What is a Z-index?_**

Z-Index(z-index) is CSS property that defines the order of overlapping HTML elements. Elements with a higher index will be placed on top of elements with a lower index.

Note: Z-index only works on positioned elements (position:absolute, positione:relative, or position:fixed).

## CSS Units

**Absolute**

- Px - Pixel
- Cm - Centimeter
- mm - milimeter
- m
- i

**Relative**

- % - Percentage
- VH - ViewportHeight
- Vw - ViewportWidth
- em - empasis
- rem - Root

## 4. What is CSS Unit

**Ans:** When we give in CSS property to Size, we will tell the browser how much we wants the size.

```
.box {
  width: 200px;
}

<!-- 200 = vlaue -->
<!-- px  = unit -->
<!-- CSS value + unit -->
```

Example:

```
font-size: 20px;
margin: 2rem;
width: 50%;
height: 100vh;
```

Understand with simple Analogy

if anyone Says:

    i want a table 5.
    **Ques** What 5? Meter? centimeter? or Feet?
    Similarly: width: 200;

## 2. Absolute vs Relative Units

We will Understand CSS length unit in two groups.

### Absolute

- Px
- cm
- mm
- in

### Relative

- %
- Vh
- Vw
- em
- rem

Main Difference:

**Absolute Unit:**
Size relatively fixed/ reference-based hota hai; Surrounding element ke size se directly scale nahi hota.

**Relative Unit**
Size kisi reference ke according calculate hota hai.

### 3. Absolute Unit

#### 3.1 px -- Pixel

px CSS most commonly used units

```
.box {
  width: 200px;
  height: 100px;
}

<!-- Width = 200px -->
<!-- height = 100px -->
```

Beginner Understanding
In Real Physical Screen with pixel 1:1 relatonship assume nahi karna chaiye, especially high-density/ zoomend displays par.

When we Use ?
px useful for

- Borders
- Small spacing
- icons
- precise dimensions
- shadows
- controlled UI details

```
button {
  border: 1px solid black;
  padding: 10px 20px;
}
```

#### 3.2 Cm -- Centimeter

Cm represents centimeter

```
.box {
  width: 5cm;
}
<!-- 5cm = 5 centimeters -->
```

In css this will be a physical measurement unit.
This will be mostly useful for

- Print styles
- physical-size documents
- print layout

```
@media print {
  .page {
    width:21cm;
  }
}
```

#### 3.3 mm -- Millimeter

mm = millimeter

```
.box {
  width:50mm;
}
<!-- 10mm = 1cm -->
```

Again, web UI mein generally px, %, rem, em, vw, vh mostly common
mm will be used to print / physical dimensions

#### in -- Inch

CSS standard unit in and its meaning was inch

```
.box {
  width : 2in;
}
<!-- 1in = 2.54cm -->
<!-- 1in = 96px -->
So conceptually
1in --> 2.54cm --> 25.4mm
```

Part B --- Relative Units
Relative units will be calculate by any reference

#### 3.4 % --- Percentage

% kisi reference / containing value ke realative hota hai.

```
.container {
  width: 500px;
}
.box {
  width: 50%;
}

if .box percentage width parent / container ke 500px reference ke according calculate

500px * 50% = 250px

so

Box =250px wide
```

Real world analogy
if you have 100rs

```
50% of 100rs = 50rs

similarly
50% of 500px = 250px
```

#### 3.5 vh --- viewport height

vh = viewport height
1vh viewport height 1%
100vh = 100% viewport height

```
.hero {
  height: 100vh;
}
 1vh = 8px

 50vh = 400px
 100vh = 800px

 .hero {
  height:100vh
 }

┌──────────────────────┐
│                      │
│       HERO           │
│                      │
│                      │
│                      │
└──────────────────────┘
       100vh
```

14. vw — Viewport Width
    vw = viewport width.

```
1vw = 1% of viewport width

Therefore:
100vw = viewport width

Example:
.section {
    width: 100vw;
}
```

15. vw Calculation
    Suppose viewport width:
    1200px

Then:
1vw = 12px

Therefore:
50vw = 600px

## 100vw = 1200px

**em**
Ab ek bahut important unit.
Tumhare notes mein:
em - emphasis

likha hai.
Correction: em ka meaning "emphasis" nahi hai.
CSS mein em ek relative length unit hai.
Its calculation depends on the font size of the relevant element/context, with details depending on which property is using em.
For font-size itself, the calculation is based on the parent's computed font size.

#### 21. rem — Root EM

rem = root em.
Yahan r ka meaning:
root

Usually browser document ka root element:

<html>

hota hai.
So rem root element ke font size ke relative hota hai.
