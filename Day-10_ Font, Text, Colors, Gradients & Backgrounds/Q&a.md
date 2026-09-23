## CSS typography --Interview Questions & Answers

## 1. Font-size

### 1. What is Font-size in Css?

**Ans:** font-size is a CSS property used to specify the size of text displayed on a webpage.

```
p {
    font-size:18px;
}
```

Here the paragraph text will have a size of 18px.

---

### 2. What is the use of Font-Size ?

**Ans:** The font-size property controls how large or small text appears.
it helps with:

- Readability
- Visual hierarchy
- Response typography
- Accessibility
- Creating different heading and paragraph sizes.

### 3. What are common units used with font-size ?

**Ans:** Common units include:

- Px
- em
- rem
- %
- vw

```
h1 {
    font-size:32px;
}

p{
    font-size: 1rem;
}
```

### 4. What is the Difference between px, em, and rem for font-size ?

**Ans:** Px

- A fixed Css pixel-based size.

**PX**

```
p {
    font-size:10px;
}
```

- Em Relative to the font size of the relevant parent/current context.

**em**

```
p {
    font-size:1.5em;
}
```

- Rem Relative to the root (html) element's font size.

**rem**

```
p {
    font-size: 1.5rem;
}
```

### 5. What is the default font size of a browser ?

**Ans:** In Common browser defaults, the root html font size is typically 16px, although user/browser settings can affect the effective result.

For Example:

```
html {
    font-size: 16px;
}
```

Then:

```
p {
    font-size: 1rem;
}
```

is typically equivalent to 16px.

### 6. What does font-size: 2rem mean ?

**Ans:** It means the font size is 2 times the root element's font size.

```
html {
    font-size: 16px;
}
```

then:

```
h1 {
font-size: 2rem;
}
```

**Means: 2 \* 16px = 32px**

## 2. Font-weight

### 7. What is font-weight in CSS?

**Ans:** font-weight is a CSS property used to control the thickness or boldness of text.

```
p {
    font-weight: bold; or
    font-weight: 700;
}
```

### 8. What values can font-weight have ?

**Ans:** Common values include:

- normal
- bold
- 100
- 200
- 300
- 400
- 500
- 600
- 700
- 800
- 900

### 9. What does font-weight: 400 mean ?

**Ans:** 400 generally represents the normal weight.

```
p{
    font-weight: 400;
    font-weight: normal;
}
```

### 10. What does font-weight: 700 mean ?

**Ans:** 700 generally represents a bold weight.

```
h1 {
    font-weight: 700;
    font-weight: bold;
}
```

### 11. What is the difference between font-weight: Bold and font-weight: 700 ?

**Ans:** Both commonly represents the same level of weight.

```
font-weight: bold;
font-weight: 700;
font-weight: 400;
font-weight: 500;
font-weight: 700;
```

### 12. Does every font support all weights from 100 to 900 ?

**Ans:** No. A font may only provide certain weights. for example, a font might provide:

## 3. Line-Height

### 13. What is line-height in CSS?

**Ans:** line-height controls the height of a line of text.
it affect the vertical spacing between lines in a block of text.

```
p {
   line-height: 1.6;
}
```

### 14. why is line-height important ?

**Ans:** Line height improves:

- Readability
- Text spacing
- Paragraph appearance
- Vertical rhythm
- Overall typography

for Example:

```
p {
    line-height: 1.6;
}
```

usually provides more comfortable paragraph spacing than a very tight line height.

### 15. What value can line-height accept ?

**Ans:** It Can accept:

**Unitless number**

```
p {
    line-height: 1.5;
}
```

**Length**

```
p {
    line-height:24px;
}
```

**Percentage**

```
p {
    line-height: 150%;
    line-height: normal;
}
```

### 16. What is the difference between line-height: 1.5 and line-height: 24px ?

**Ans:**

```
font-size:16px;
line-height:1.5;

<!-- the computed line-height is effectively: 16 * 1.5 24px -->
```

### 17. Why is unitless line-height often recommended?

**Ans:** Because is scales naturally when the font size changes and is generally easier to maintain.

```
body {
    line-height: 1.5;
}
```

If a child has a larger font size, its line height scales accordingly.

### 18. What is the difference between font-size , font-weight , and line-height ?

**Ans:**

PROPERTY | PURPOSE

FONT-SIZE | Controls text size

FONT-WEIGHT | Controls line spacing/line box height

```
P {
    font-size: 16px;
    font-weight: 400;
    line-height: 1.6;
}
```

### 19. What does this CSS code do ?

```
P {
   font-family: Arial , sans-serif;
   font-size: 16px;
   font-weight: 400;
   line-height: 1.6;
}
```

**Ans:**
it Specifies:

- font-family -> Arial, with a sans-serif fallback
- font-size -> 16px
- font-weight -> normal/400
- line-height -> 1.6 times the font size

So the effective line-height is approximately: 16 \* 1.6 = 25.6px

### 20. You want a heading to be 32px and bold. How would you write it ?

**Ans:**

```
h1 {
    font-size: 32px;
    font-weight: 700;
}
```

### 21. You want paragraph text to be 16px with comfortable spacing between lines what would you write ?

**Ans:**

```
p {
    font-size: 16px;
    line-height: 1.6;
}
```

### 22. How would you make text smaller without changing the font familly ?

```
P {
    font-size: 14px;
}

<!-- font-size changes the text size while leaving the font family unchanged. -->
```

### 23. How would you make text thicker without changing its size ?

**Ans:**

```
p {
    font-weight: 700;
}

    <!-- The font-weight changes the thickness, while font-size remains unchanged. -->

```

### 24. How would you increase the space between lines without making the text bigger?

**Ans:** Use Line-Height

```
p {
    font-size: 16px;
    line-height: 1.8;
}

<!-- The text remains 16px, while the line spacing increases. -->
```

### 25. Is Line-height the same as margin between lines?

**Ans:** No. Line Height controls the line box height and affects how text lines are vertically spaced.

**margin** controls the space outside an element.

```
p {
    line-height: 1.6;
    margin-bottom: 20px;
}
```

- line-height -> Spacing within the paragraph's lines

- margin-bottom -> space after the paragraph

### 26. What happens if line-height is smaller than font-size?

**Ans:** The line boxes can become smalled than the font's normal glyph area, causing lines to appear very tightly packed and potentially overlap visually.
Ex:

```
p {
    font-size: 30px;
    line-height: 0.8;
}

<!-- This is usually undesirable for normal paragraph text. -->
```

### 27. Can line-height be inherited?

**Ans:** Yes. Line-height is an inherited property.

```
body {
    line-height: 1.5;
}

Child elements can inherit that value.
A unitless value is particularlt useful because it scales with the child's own font size.
```

### 28. What is a good line-height for body text ?

**Ans:** There is no universal value, because it depends on the font, size, width, and design.
A common starting point for body text is around:

```
line-height: 1.5;
line-height: 1.7;

THen adjust based on readability and design.
```

### 29. Can font-size be responsive?

**Ans:** Yes

```
h1 {
    font-size: 5vw;
}

h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}

<!-- clamp() allowa a minimum, preferred, and maximum size. -->
```

### 30. What is Clamp() in responsive typography?

**Ans:** Clamp() allows you to define a minimum, preferred, and maximum value.

```
h1 {
    font-size: clamp (2rem, 5vw, 4rem);
}
2rem -> minimum
5vw  -> preferred fluid value
4rem -> maximum

<!-- This is useful for responsive headings. -->
```

### 31. Which property controls text size?

**Ans:** Font-Size

### 32. Which property controls text thickness?

**Ans:** Font-weight

### 33. Which property controls the spacing/height of text lines?

**Ans:** line-height

### 34. what is the usual numeric value for normal font weight?

**Ans:** 400

### 35. what is the usual numeric value for bold?

**Ans:** 700

### 36. Is line-height: 1.5 1.5px?

**Ans:** No. it is a unitless multiplier, not 1.5 px.

### 37. What does 1rem usually represent?

**Ans:** the font size of the root (html) element.

### 38. Which is generally more scalable for line-height: 1.5 or 24px ?

**Ans:** A unitless value such as 1.5, because it scales with the element's font size.

## 3.CSS Color & Background

- Color
- RGBA
- HEX
- HSL
- Linera-gradient()
- Background-image

## 39. CSS Color

### 39. What is the color property in CSS?

**Ans:** The color property in CSS is used to define the color of the text content of an element.

### 40. How can we specify colors in CSS?

**Ans:** Css Supports several color formats, including:

```
<!-- Named color -->
color:red;

<!-- HEX -->
color:#ff0000;

<!-- RGB -->
color:rgb(255,0, 0);

<!-- RGBA -->
color:rgba(255, 0, 0, 0.5);

<!-- HSL -->
color: hsl(0, 100%, 50%);
```

### 41. What is HEX color in CSS?

**Ans:** A Hex color is a hexadecimal representation of a color in CSS. it usually consist of six hexadecimal digits preceded by a # Symbol.

### 42. How does a HEX color work?

**Ans:** A normal 6-digit HEX color has three pairs:

**#RRGGBB**

Where:

-- RR -> Red

-- GG -> Green

-- BB -> Blue

### 43. What does #000000 represent?

**Ans:** **White** Color:ffffff;

### 44. What is the short form of HEX color?

**Ans:** Some 6-Digit HEX colors can be shortened to 3 digits.

for example:

```
#ffffff
#fff
#ff0000
#f00
```

### What is RGBA?

**Ans:**

```
R --> Red
G --> Green
B --> Blue
A --> Alpha

<!-- Alpha transparency/opacity ko control -->

P{
    color: rgba(255, 0, 0, 0.5);
}

In here Red color transparency 0.5
```

RGBA is a color notation consisting of red, green, blue and alpha channels. the alpha value controls the transparency of the color.

### What is the range of the alpha value?

**Ans:** In modern CSS syntax, alpha can be represented from:
0 --> completely transparent
1 --> completely opaque

Ex:

```
<!-- Comp -->
color: rgba(255, 0, 0, 0);
color: rgba(255, 0, 0, 1);
```
