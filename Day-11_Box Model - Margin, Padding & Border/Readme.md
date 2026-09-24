## Lecture 11 CSS Box Model - Margin, Padding & Border

- Content
- Padding
- border
- margin
- box-sizing:
- Border-box
- outline

---

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
