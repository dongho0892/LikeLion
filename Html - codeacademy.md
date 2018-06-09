# Html - codeacademy

### [Learn HTML: Elements and Structure] 

```html
<p> “Hello World!” </p> 
element   content   element


<body>
  <p>What's up, doc?</p>
</body>


<body>
  <p> This paragraph is a child of the body element</p> <!--  body 안의 <p> -->
    </p> 
  <h1>Hello World</h1>
  <div>
    <p> This paragraph is a child of the div element</p> <!--  div 안의 <p> -->
  </div> 
</body>
```



#### Headings				

```html
<body>
  <h1>The Brown Bear</h1>
  <h2>About Brown Bears</h2>
  <h3>Species</h3>
  <h2>Habitat</h2>
  <h3>Countries with Large Brown Bear Populations</h3>
  <h3>Countries with Small Brown Bear Populations</h3>
  <h2>Media</h2>
  <h1> BREAKING NEWS </h1>
</body>

```



#### Divs - is short for "division" or a container that divides the page into sections. / grouping elements 

```html
<body>
  <h1>The Brown Bear</h1>
    <div> 
  		<h2>About Brown Bears</h2>
  		<h3>Species</h3>
  		<h3>Features</h3>
    </div>
  	<div>
  		<h2>Habitat</h2>
  		<h3>Countries with Large Brown Bear Populations</h3>
  		<h3>Countries with Small Brown Bear Populations</h3>
  	</div>
</body>
```



#### Attributes - are content added to the opening tag of an element 

- The *name* of the attribute
- The *value* of the attribute

```html
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h1>Introduction</h1>
    <h2>About Brown Bears</h2>
    <h3>Species</h3>
    <h3>Features</h3>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
  </div>
  <div id="media">
    <h2>Media</h2>
  </div>
</body>
```

#### Displaying Text

- *Paragraphs* (`<p>`) contain a block of plain text.
- `<span>` contains short pieces of text or other HTML.
- `<span>` element when **you want to target a specific piece** of content that is *inline*, or on the same line as other text. 
- If you want **to divide your content** into *blocks*, it's better to use a **`<div>`.** 

```html
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (Ursus arctos) is native to parts of northern Eurasia and North America. Its conservation status is currently Least Concern. There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
```



#### Styling Text

* `<em>` tag emphasizes text					-*italic* emphasis. 
* `<strong>` tag highlights important text.          -**bold** emphasis. 

```html
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>. There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <h3>Features</h3>
  </div>
</body>
```



#### Line Breaks

* HTML's *line break* element: `<br>`. 



#### Unordered Lists

* `<ul>` to create a list of items in **no particular order.** (특별한 순서 없이)

  ​	(unordered list)

* + `<li>` or list item tag is used to describe an item in a list. 

```html
<body>
  <div>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
  </div>
</body>
```



#### Ordered Lists

* `<ol>` are like unordered lists, except that **each list item is numbered** 
* + `<li>` or list item tag is used to describe an item in a list. 

```html
<body>	
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>		
      <li>Canada</li>
    </ol>
  </div>
</body>
```



#### Images

* `<img>` tag allows you to add an image to a web page.  
* Note that the end of the `<img>` tag has a forward slash `/`.
* + has a required *attribute*called `src` 

```html
<body>
  <div id="media">
    <h2>Media</h2>
    <img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/web101-image_brownbear.jpg"/>
  </div>
</body>
```



##### Image Alts

* The `alt` attribute, which means alternative text, brings meaning to the images on our sites
* * If an image fails to load on a web page, a user can mouse over the area originally intended for the image and read a brief description of the image.  
  * When you include the `alt` attribute, the screen reading software can read the image's description out loud to the visually impaired user. 
  * The `alt` attribute also plays a role in Search Engine Optimization (SEO), because search engines cannot "see" the images on websites as they crawl the internet. 

````html
<body>
  <div id="media">
   	<h2>Media</h2>
   	<img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/web101-image_brownbear.jpg" alt="brown bear"/>
  </div>
</body>
````



##### Videos

* HTML also supports displaying videos. Like the `<img>` tag, the `<video>` tag requires a `src` attribute with a link to the video source. 
* * the `<video>` element requires an opening and a closing tag. 
  *  The `controls` attribute instructs the browser to include basic video controls: pause, play and skip. 
  * between the opening and closing video tags will only be displayed if the browser is unable to load the video.               # <video> ~~~   실행이 안됩니다. </video>

````html
<body>
	<div id="media">
   		<h2>Media</h2>
    	<img src="https://s3.amazonaws.com/codecademy-content/courses/web-101/web101-image_brownbear.jpg" alt="A Brown Bear"/>
        <video src="https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>
          Video not supported
    	</video>
  	</div>
</body>
````



# Review

* **HTML** stands for **H**yper**T**ext **M**arkup **L**anguage and is used to create the structure and content of a webpage.
* Most HTML elements contain opening and closing tags with raw text or other HTML tags between them
* HTML elements can be nested inside other elements. The enclosed element is the child of the enclosing parent element.
* Any visible content should be placed within the opening and closing `<body>` tags .
* Headings and sub-headings, `<h1>` to `<h6>` tags, are used to enlarge text.
* `<p>`, `<span>` and `<div>` tags specify text or blocks.
* The `<em>` and `<strong>` tags are used to emphasize text.
* Line breaks are created with the `<br>` tag.
* Ordered lists (`<ol>`) are numbered and unordered lists (`<ul>`) are bulleted.
* Images (`<img>`) and videos (`<video>`) can be added by linking to an existing source.