# html basics
### HTML: hyper text markup language
* **html** is a standardized **markup language** for writing webpages.<br>
* **markup languages** are used to annotate a document in a way that is *syntactically distinguishable* from the text. (this document was written in the markup language **markdown**) 
* **hypertexts** are texts which *link* to other texts. (sometimes called **hypermedia** when referring to *networked media* other than text like video or images).


### what *is* an HTML document?
HTML documents are plaintext documents that end in the extension `.html`. HTML documents consist of a standard structure of **elements** that can be recognized and rendered by all modern browsers. HTML documents are styled through **Cascading Style Sheets**, or **CSS**. These use the extension `.css`. An HTML document knows what stylesheet to use through a **link**... more on that later.
HTML documents are transmitted across networks through **HTTP requests**. Your browser will **request** a webpage from an **IP address** (an Internet Protocol address (IP address) is a numerical label assigned to each device (e.g., computer, printer) participating in a computer network communicating through the Internet), then the associated server will send back the requested HTML page.

##### the basic skeleton of an HTML page
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>My HTML Page</title>
  <link rel="stylesheet" href="MyStylesheet.css" type="text/css">
  </head>
  <body>
  
  </body>
</html>
```

the first line of the code, `<!DOCTYPE html>` just declares that the following document will be written in HTML. after that, the rest of the document is **nested** inside a single set of `<html>` tags.
at this point our HTML is split into 2 sections, the `<head>` and the `<body>`. 
###### the head
Between the `<head></head>` tags we put fairly obligatory information like the **charset** or character set of the text, the **title** of the page and a link to the **stylesheet** for your page. if you import fonts from **Google Fonts** or use **Javascript** files in your page, you would also link to them in this section.<BR>
***IMPORTANT:** Nothing in the `<head>` section will be rendered on the actual HTML page. this is just information for how the page will be rendered and accessed by browsers and databases.*
###### the body
the actual content of your webpage lives between the 
`<body>` tags. here are some standard HTML elements you can use to organize your content within the body:

* `<p></p>` is used to enclose paragraphs.
* `<a href="http://my-link.org">my link</a>` is used to create links to other web pages.
* `<h1,2,3...6></h1,2,3...6>` is used do do different sizes of heading text. for example, the largest heading size would be `<h1>` and the smallest is `<h6>`.
* `<img src="http://my-site.org/image3.png" alt="Image 3" width="100" height"100">`embeds images in the page. the **alt** attribute is for text to be used if the image can't be loaded or for people using Accessibility Services to listen to the website. Width and height are self-explanatory. the src or source attribute is the only
required one; the rest are optional.

some elements are a bit more complicated--for example, the `<video>` and `<audio>` elements.
here is a typical use of the `<video>` element:

```
<video width="320" height="240" autoplay>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
```
You probably recognize some of the attributes from the image tag, like src and width/height. however, things are structured a bit differently with video. for example, you can use the **autoplay** attribute to make the video start playing automatically. additionally, the source URLs are nested inside the video element in `<source>` tags and paired with unique **types**. this is so that your browser picks the right video format for your computer. If all else fails, it will display the text instead.

the `<audio>` element works similarly.

```
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
```

the **controls** attribute means that transport controls (play, pause, etc) will be displayed on the page. **controls** can be used with the video element as well, just as **autoplay** can be used with audio. other attributes you can use include **loop**, **muted** and **preload**.

### CSS

if you wrote your whole website in just HTML, it would work just fine but it would look really ugly-- without custom CSS, websites are usually just rendered in Times New Roman on a white background, left-aligned. instead, we can write a **style sheet** to make our website look however we want it to!

here's the standard syntax for stylesheets:

```

body {
	background-color: blue;
	font-family: Helvetica, Arial, sans-serif;
}

p {
	font-size: 12px;
}

a {
	text-decoration: none;
	color: yellow;
}

a:hover {
	background-color: red;
}

```

this would display our website with a blue background and using the font Helvetica. our main `<p>` text would be 12 pixels high and our links would be yellow and have no underline--when we **hover** over them with the mouse, they would get a red highlight.

There's a lot more you can do with HTML and CSS, but this should be enough information to get you started without feeling too overwhelmed.

:)