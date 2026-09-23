# Lecture 10 CSS Font, Text, Colors, Gradients & BackGrounds

- font-familly
- Font-Size
- Font-Weight
- Line-height
- Color
- RGBA
- HEX
- HSL
- Linear-gradient
- Background-image

---

## Font-Family
### 1. What is Font-family in CSS?

Ans: Font-family Css property used to specify the typeface or font familly that shoult be used to display text.

---

### 2. What is the use of font-familly?

Ans: The Font-family property is used to control the appearance of text by specifying which font should be used.

---

### 3. What is the syntax of font-familly?

Ans:

```
Selector{
  font-family: font-name;
}

h1 {
  font-family: "Courier New", Courier, monospace;
}
```

---

### 4. Can we Specify multiple fonts in font-familly?

Ans: Yes. We can specify multiple fonts separated by commas. these are callled fallback fonts.

---

### 5.Why do we use multiple fonts in font-family?

Ans: We use multiple fonts as a fallback mechanism. if the fist font is unavailable, the browser tries the second font. if the second is unavailable, it tries the next one.

---

## Font-Size
```
p{
  font-familly: Arial, Helevetica, Sans-serif;

},
h2 {
  font-size: 25px;
}
```

---

### 6.What is a Fallback Fonts?
Ans: A Fallback font is an alternative font that the browser uses when the preferred font is unavailble.

---

### 7.What are generic font families in Css?
Ans: Generic font families are broad categories of fonts that browsers can use when a specific font isn't available.

common generic families are:

- Serif
- sans-serif
- monospace
- cursive
- fantasy
  -system-ui

---

### 8.What is the difference between a font family and a specific font?
Ans: A Specific font refers to a Particular typeface, such as arial or georgia.

---

### 9.What happens if the Specified font is not installed on the user's computer?
Ans: if the specified font is unavailable, the browser moves to the next font in font-family list.

---

### 10.What is the difference between serif and sans-serif?
Ans: Serif fonts have small decorative strokes at the ends of letters.

---

### 11.Why should we include a generic familly at the end of a font list?
Ans: It Provides a final fallback if none of the preferred fonts are available

---

### 12.When Should quotation marks be used around a font name?
Ans: Quotation marks are commonly used when the font name contains spaces or multiple words.

---

### 13.Is font-familly case-sensitive?
Ans: font family names are generally matched without case senstivity.

## Font-Weight
```
h3 {
  font-weight: 900;
}
```

## Line-Height
```
h4 {
  line-height: 2;
}
```

## Font Style & Variance

```
h2{
    font-style: italic;
    font-variant: Small-caps;
}
```

## Letter-Spacing

```
h2{
    letter-spacing: 25px;
}
```

## Word-Spacing

```
word {
    word-Spacing: 25px;
}
```

## Text-Properties

```
Text{
    text-align: center; end; justify;

    text-decoration: underline; dashed; dotted; double; line-through; overline; wavy

    text-transform: Capitalize; lowercase; uppercase;

    text-indent: 39px;

    text-shadow: 10px 10px 10px  [X axis  y axis Blur color]
}
```

## Color Property there are 4 type for give Color property

### Named Colors

```
#color{
  color: cyan;
  color: red;
}
```

### HEX Hexadecimal Code

          R     G     B
       # _ _ , _ _ , _ _

       # 0 0 , 0 0 , 0 0  -> Black
       # f f , f f , f f  -> White
       # f f , 0 0 , 0 0  -> Red
       # 0 0 , f f , 0 0  -> Green
       # 0 0 , 0 0 , f f  -> Blue

### RGB / RGBA

#### RGB

- R means Red Colors
- G means Green Colors
- B means Blue

```
RGB Color{  0-255
 color: rgb(red, green, blue);
 color: rgb(255, 255, 255);
}
```

---

#### RGBA

- R means Red Colors
- G means Green Colors
- B means Blue Colors
- A means Alpha for Blur

```
RGBA Color{
 color: rgba(245, 0, 255, 2)
}
```

## HSL / HSLA

### HSL

- Hue means Color
- Saturation means Level
- Light means Brightness
- A means Alpha for Blur

```
HSL Color{
color: hsl(360, 100% , 50%)
color  hsla(360, 100%, 50% , 5)
}
```

## Q & A

### 14. Can font-family accept a custom font?

Ans: We can load a custom font using font-face and then use it with font-family.

```
@font-face{
  font-family: "MyFont";
  src: url("myfont.woff2");
}

body{
  font-familly: "MyFont", sans-serif;
}
```

### 15. What is @Font-face?

Ans: @font-face is a Css rule that allows developers to define and use custom fonts in a webpage.

```
@font-face{
  font-family: "myFont";
  src: url ("myfont.woff2");
}
```

### 16. What is Wrong with this Code?

```
body{
  font-family: Arial;
}
```

**Ans:** Nothing is technically wrong. However, it's generally better to provide fallback fonts.

Better.

```
body{
  font-family: Arial, sans-serif;
}
```

### 17. What does this mean?

```
font-familly:"Helvetica Neue", Helvetica, Arial, Sans-serif;
```
Ans: the browser tries the fonts in this order:
- Helvetica Neue
- Helvetica
- Arial
- any available sans-serif font
the first available option is used.

### 18. What happens if all fonts in a font-family list are unavailable?
Ans:
 The browser selects an appropriate font based on its default font setting and the generic family, if one was provided.
For example:
```
font-family: "Unknown font", sans-serif;
```
if the names font doesn't exist, the browser uses an available sans-serif font.

### 19. How can you apply a font to the entire webpage?
**Ans:**

```
body{
  font-family: Arial, sans-serif;
}
```

### 20. Does font-familly inherit?
**Ans:** font-family is an inherited Css property.
Ex:
```
body{
  font-family: Arial, sans-serif;
}
```
A child element will normally inherit this font unless it specifies another font-family.

### 21. What is the difference between font-family and font-size?
Ans: font-family determine which typeface is used.
```
P{
  font-family:Arial;
}
```
font-size determines how large the text is.
```
P{
  font-size:20px;
}
```

### 22. What is the difference between font-family and font-style?
**Ans:** font-family chooses the typeface:
```
P{
  font-familly: Arial;
}
```
font-style controls the style, such as normal or italic:

```
p{
  font-style:italic;
}
```
### 23. What is the difference between font-family and font-weight?
**Ans** font-family determines the typefaces.
```
font-family:Arial;
```
fonts-weight controls the thickness of the text.
```
font-weight:700;
```

### 24. What is font stack?
**Ans** A font stack is a list of fonts specifies in font-family, arranged in order of preference.
```
body{
  font-family:"segoe UI, Arial, sans-serif;
}
the browser checks each font left to right.
```

### 25. Why is sans-serif usually placed at the end of a font stack?
**Ans** Because it acts as a generic fallback.
```
font-family: "Roboto", Arial, sans-serif;
```
if Roboto and arial are unavailable, the browser can still select an available sans-serif font.

### 26.Can we use font-family with web fonts?
**Ans:**  Yes.
For Example
```
@font-face{
  font-familly: "MywebFont";
  src: url("font.woff2") format("woff2");
}

h1{
  font-familly:"MyWebFOnt", sans-serif
}
```
### 27. What font format is commonly recommended for modern web fonts?
**Ans** Woff2 is commonly preferred for modern web usage because it provides efficient compression and broad modern-browser support.
```
@font-face{
  font-family: "MyFont";
  src: url("myfont.woff2") format("woff2");
}
```

### 28. What is the DIfference between a named font family and a generic family?
**Ans** A named font familly refers to a particular font family:
```
font-family:Arial;
- sans-serif
- monospace
- cursive
- fantasy
- system-Ui
```

### 29. Why Should developers avoid relying on only one specific font?
**Ans** Because the font may not be available on every user's device or operation system.
```
font-family:Arial;
```
developers can use:
```
font-family: Arial, helvetica, sans-serif;
```

### 30. What is a system font stack?
**Ans:** A system font stack uses fonts that are already available on the user's operating system.
```
body{
  font-family:system-ui, sans-serif;
}
```

### 31. You want the website to use Roboto, but if Roboto isn't available, use Arial. How would you write it?
**Ans:** 
```
body{
  font-family:Roboto, Arial, sans-serif;
}
```

### 32. You want a heading to use Georgia and a paragraph to use Arial. How would you do it?
**Ans:**
```
h1{
  font-family:Georgia, serif;
}
p{
  font-family: Arial, sans-serif;
}
```

### 33. Your custom font isn't loading. what would you check?
**Ans:**
I would Check:
- Whether the font file path is correct.
- Whether the font file exists.
- Whether @font-face is written correctly.
- Whether the font format is supported.
- Whether the browser console shows an error.
- Whether the server is correctly serving the font file.
- Whether CORS configuration is required for a cross-origin font.

### 34. Why might a browser display a diifferent font than the one specified?
**Ans:**
Possible reasons include:
- The specified font isn't available.
- The font failed to load.
- The font file path is incorrect.
- The web font request failed.
- A fallback font was used.
- Another Css rule has higher specificity or later precedence.

### 35. Can font-family contain more than one font?
**Ans:** Multiple fonts can be specified as a comma-separated list.
```
font-family: "Roboto", Arial, Helvetica, sans-serif;
```

### 🎯 Most Important Questions to Prepare
- What is font-family ?
- What is its purpose ?
- What is the syntax ?
- Can we specify multiple fonts ?
- What is a fallback font ?
- What is a font stack ?
- What are generic font families ?
- Difference between serif and sans-serif ?
- Why do we use sans-serif at the end ?
- Does font-family inherit ?
- How do you use custom fonts ?
- What us @font-face ?
- Difference between font-family, font-size, font-style, and font-weight ?
- What happens when a font isn't available ?
- How would you troubleshoot a font that isn't loading ?