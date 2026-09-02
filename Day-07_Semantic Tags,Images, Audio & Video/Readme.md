# Sematic Tag

Semantic Means meaning

## Layout of Website

- Header
- Main
- Aside
- Footer

## Non- Semantic Tag

- Div
- Span

## Semantic Tag

- Header
- nav
- main
- article
- section
- aside
- footer

---

### Header

header is Showing our head section in our webppage

---

### nav

Navbar is using for our navigation link

---

### main

in this tag where our main content heres

---

### article

Is for writing information about product or like Blog Newspaper or some articles in one products information contains in this Tag.

---

### Section

section for dividing our content in many parts.

---

### Aside

Aside tag is using for our sidebar contents like in our webpage in the main content of the side bar we showing our sidebar

---

### Footer

footer is for showing our information of webpages like contact us email id and this is showing in bootom of our webpage.

---

## Media Tag

- Image
- Video
- Audio

---

### Image Tag

image tag is using for showing an image in our webpage.

---

### Figure & Caption Tag

figure is for our image container and caption is for showing our images caption

### Images Src and Alt Attributes

src uses for from our links or path the image wheres comes from ?

Alt att uses for if any cases the image not showing in our webpage so we are writing an image content name that was appear on the images sides.

---

## Video Tag

Video tag is using for showing an video and play in our webpage like Youtube.

### Video Tag Attributes

Src atbr for add the path from where comes our video and height and width for in our webpage screen size adjust height for heigth adjust and width for width adjustment and control tag is for control our video in our webpage like pause seek forward play and mute for mutes video play and loop for our video never play in ends.

```
        <video
          src="Rolling dice.mp4"
          width="400px"
          height="300px"
          controls
        ></video>
```

---

### Audio Tag

Audio Tag is Using for audio file in our webpage in this tag we are play any audio file.

```
<audio src="audio.mp3" controls></audio>
```

---

### Iframe Tag

In Someone content showing in our webpages or map video for this.

```
        <iframe>
          src="https://www.google.com/maps/embed?pb=!1m24!1m12!1m3!1d6999.88877980504!2d76.92093721461741!3d28.691310063346712!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m9!3e6!4m3!3m2!1d28.7116208!2d76.9304274!4m3!3m2!1d28.6873346!2d76.9255034!5e0!3m2!1sen!2sin!4v1788269963401!5m2!1sen!2sin"
          width="600"
          height="450"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="strict-origin-when-cross-origin"
        </iframe>

```

### HTML Comments

In html code we are writing notes for understanding what this code do and its for other developer understanding. for writing a comments.
Ctrl + / key for make comments.

```
<!-- this is Html Comments -->
```

## HTML ENTITIES

Html Entities is for showing reserved code or Special code

---

- for non-breaking space

```
&nbsp;   &#160;
```

---

- for&nbsp; < &nbsp;less than sign

```
&lt;     &#60;
```

---

- for&nbsp; >&nbsp; greater than sign

```
&gt;     &#62;
```

---

- for &nbsp; & &nbsp; Ampersand

```
&amp;    &#38
```

---

- for&nbsp; " &nbsp; Double Quotation mark

```
&quot;   &#34;
```

---

- for &nbsp; &nbsp; ' &nbsp; &nbsp; Single Quotation mark

```
&apos;   &#39;
```

---

- for&nbsp; ¢&nbsp; cent mark

```
&cent;   &#162;
```

---

- for&nbsp; £&nbsp; pound mark

```
&pound;  &#163;
```

---

- for&nbsp; ¥ &nbsp; yen mark

```
&yen;    &#165;
```

---

- for&nbsp; € &nbsp; euro mark

```
&euro;    &#163;
```

---

- for&nbsp; © &nbsp; copyright mark

```
&copy;    &#169;
```

---

- for&nbsp; ® &nbsp; registered trademark

```
&reg;     &#174;
```

---

- for&nbsp; ™ &nbsp; trademark

```
 &trade;   &#8482;
```

---

## Personal Portfolio

Chand Ansari | Simple Portfolio

```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Chand Ansari | Portfolio</title>
  </head>
  <body>
    <header>
      <h1>Chand Ansari</h1>
      <p>Full Stack Developer & Lifelong Learner</p>
      <nav>
        <a href="#About">About</a>
        <a href="#Projects">Project</a>
        <a href="#Contact">Contact</a>
      </nav>
    </header>

    <main>
      <section id="About">
        <h0000>About Me</h0000>
        <figure>
          <img src="https://picsum.photos/200/300" alt="Lorem" />
          <figcaption>That's me at my first hackathon!</figcaption>
        </figure>
        <p>
          Hi! I am <strong>Chand Ansari</strong>, a passionate full stack
          developer learning to build real-world products. I am currently taking
          the <em>PW full stack Course.</em>
        </p>
      </section>

      <section id="Projects">
        <h2>My Projects</h2>
        <article>
          <h3>Project One : Portfolio Website</h3>
          <p>
            A Simple personal portfolio built with <strong>HTML & CSS.</strong>
          </p>
          <a href="">View on Github</a>
        </article>

        <article>
          <h3>Project Two : Todo App</h3>
          <p>
            A todo list app built with built with <strong>JavaScript.</strong>
          </p>
          <a href="">View on Github</a>
        </article>
        <div>
          <h3>Skills</h3>
          <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
          </ul>
        </div>
      </section>

      <section>
        <h2>Watch My Intro</h2>
        <video src="Dice.mp4" width="700px" height="300px" controls></video>
      </section>
    </main>

    <footer id="Contact">
      <h2>Contact Me</h2>
      <p>
        Email :
        <a href="itschandansari@gmail.com" target="_blank"
          >itschandansari@gmail.com</a
        >
      </p>
      <p>
        Phone : <a href="tel: +9181990240108" target="_blank">9876543210</a>
      </p>

      <form action="">
        <label for="name">Name: </label>
        <input type="text" id="name" />
        <br />
        <br />

        <label for="Email">Email :</label>
        <input type="email" name="Email" id="" />

        <br />
        <br />
        <label for="Message">Message :</label>
        <br />
        <textarea name="Message:" id="message" rows="4" cols="30"></textarea>
        <br />
        <button type="submit">Send Message</button>
      </form>
      <p>&copy; 2026 Chand Ansari, All rights reserved.</p>

      <a href="Linkdln.com">Linkdln</a> |
      <a href="Github.com">Github</a>
    </footer>
  </body>
</html>

```
