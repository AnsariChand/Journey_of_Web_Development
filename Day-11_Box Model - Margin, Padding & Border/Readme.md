## Lecture 11 CSS Box Model - Margin, Padding & Border

- Content
- Padding
- border
- margin
- box-sizing:
- Border-box
- outline

---

### 1. What is the CSS Box Model?

**Ans:** CSS Box Model ek fundamental concept hai jo explain karta hai ki browser kisi html element ki size, spacing aur boundaries ko kaise calculate karta hai.

### Background Color

```
h1{
    background-color: brown;
}
```

### Gradient

Mixture of Colors
There are three type pf Gradient

**Liner-Gradient**

```
 Background: linear-gradient(to right, red,blue);

 Background: linear-gradient(to top, red,blue);

 Background: linear-gradient(to left, red,blue);

 Background: linear-gradient(45deg, red, blue, yellow, pink);
```

**Radial-Gradient**

```
Background:radial-gradient(circle, red, green);
```

**Conic-Gradient**

```
Background:conic-gradient(red, yellow, green);
```

**Background Image**

```
background-image: url(https://picsum.photos/200/300
);
.wrapper {
  background-image: url(https://picsum.photos/200/300);
  height: 1500px;
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
}
```

## Box-Model

content Text or Image --> Padding --> Border --> margin

- **Content**

---

- **Border**

  Width, style color, radius

```
border-width: 20px;
border-style: solid;
border-color: red;
border: 2px solid navy;
border-radius: 50%
border-top-left-radius: 0;
```

- **Padding**

  Space between border and content

Top right bottom left

Top/bottom | left/right

```
padding: 40px
padding: 1px solid red;
padding: 0 40px 0 40px;
padding: 0 40px
```

- **Margin**

  Space between elements

```
margin: auto;


```

**Related Concepts**
What Should you know before Box Model?
HTML Elements -->
Css Slectors -->
Css Properties -->
Width & Height -->
Css Box Model -->

---

After Box Model?

Box Model -->
Display -->
Block vs Inline -->
Position -->
Flexbox -->
Css Grid -->
Responsive Design -->

**Commonly Confused**
Padding --> Inside Space
Margin --> Outside Space
Border --> Boundary around element
Outline --> Visual line Outside box
Width --> Content width by default
box-sizing --> Controls width/ Height Calculation
