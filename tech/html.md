This comprehensive HTML Cheat Sheet is an essential resource for both beginners and seasoned developers. It covers everything from basic HTML structure, like creating your first "Hello World" page, to detailed explanations of form handling, semantic HTML5 tags, accessibility features, and modern web development practices. Additionally, it includes a section on deprecated tags and attributes, guiding users towards using modern CSS and HTML5 alternatives for better functionality and compliance with web standards. Whether you're learning HTML for the first time or brushing up on the latest web technologies, this cheat sheet offers valuable insights and links to further enhance your web development skills.

## Getting Started
### hello.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5 Hello World</title>
</head>
<body>
    <h1>Hello world!</h1>
</body>
</html>
```

### Comment

```html
<!-- this is a comment -->

<!--
    Or you can comment out a
    large number of lines.
-->
```


### Paragraph

```html
<p>I'm from cheatsheets.one</p>
<p>Share quick reference cheat sheet.</p>
```
See: [The Paragraph element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)




### HTML link

```html 
<a href="https://cheatsheets.one">CheatSheets</a>
<a href="mailto:jack@abc.com">Email</a>
<a href="tel:+12345678">Call</a>
<a href="sms:+12345678&body=ha%20ha">Msg</a>
```
---

|   |          |                                                                 |
|---|----------|-----------------------------------------------------------------|
|   | `href`   | The URL that the hyperlink points to                            |
|   | `rel`    | Relationship of the linked URL                                  |
|   | `target` | Link target location: <br/>`_self`, `_blank`, `_top`, `_parent` |
{.left-text}

See: [The <a> Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#attributes)


### Link Relations (`rel` Attribute)

The `rel` attribute defines the relationship between the current document and the linked document. It's used within `<a>`, `<link>`, and `<area>` elements.

#### Common Uses

- **`alternate`**: Alternative version of the document.
- **`author`**: Link to the author's information.
- **`canonical`**: Preferred URL for content with duplicate pages.
- **`nofollow`**: Instructs search engines not to follow the link.
- **`noopener`**: Blocks access to the `window.opener` object, enhancing security.
- **`noreferrer`**: Similar to `noopener`, also prevents the HTTP Referer header.
- **`stylesheet`**: Links to an external CSS stylesheet.

### Examples

```html
<link rel="stylesheet" href="style.css">
<a href="https://example.com" rel="nofollow noopener noreferrer" target="_blank">External Link</a>
```



### Image Tag

```html
<img loading="lazy" src="https://xxx.png" alt="Describe image here" width="400" height="400">
```
---

|   |           |                                          |
|---|-----------|------------------------------------------|
|   | `src`     | Required, Image location (URL \| Path)   |
|   | `alt`     | Describe of the image                    |
|   | `width`   | Width of the image                       |
|   | `height`  | Height of the image                      |
|   | `loading` | How the browser should load              |


See: [The Image Embed element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img)



### Text Formatting Tags

```html
<b>Bold Text</b>
<strong>This text is important</strong>
<i>Italic Text</i>
<em>This text is emphasized</em>
<u>Underline Text</u>
<pre>Pre-formatted Text</pre>
<code>Source code</code>
<del>Deleted text</del>
<mark>Highlighted text (HTML5)</mark>
<ins>Inserted text</ins>
<sup>Makes text superscripted</sup>
<sub>Makes text subscripted</sub>
<small>Makes text smaller</small>
<kbd>Ctrl</kbd>
<blockquote>Text Block Quote</blockquote>
```


### Headings
```html
<h1> This is Heading 1 </h1>
<h2> This is Heading 2 </h2>
<h3> This is Heading 3 </h3>
<h4> This is Heading 4 </h4>
<h5> This is Heading 5 </h5>
<h6> This is Heading 6 </h6>
```
You should only have one h1 on your page


### Section Divisions

|                 |                                      |
|-----------------|--------------------------------------|
| `<div></div>`   | Division or Section of Page Content  |
| `<span></span>` | Section of text within other content |
| `<p></p>`       | Paragraph of Text                    |
| `<br>`          | Line Break                           |
| `<hr>`          | Basic Horizontal Line                |

These are the tags used to divide your page up into sections



### Inline Frame
```html
<iframe src="https://www.google.com/maps/d/embed?mid=1Tgt7LHg95LcpnKNxNFUSIWJS-DU&hl=en&ehbc=2E312F" width="320" height="240"></iframe>
```

See: [The Inline Frame element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)


### JavaScript in HTML

```html
<script type="text/javascript">
    let text = "Hello cheatsheets.one";
    alert(text);
</script>
```


#### External JavaScript

```html
<body>
    ...
    
    <script src="app.js"></script>
</body>
```


### CSS in HTML

```html
<style type="text/css">
    h1 {
        color: purple;
    }
</style>
```

#### External stylesheet

```html
<head>
...
<link rel="stylesheet" href="style.css"/>
</head>
```



## HTML5 Tags
### Document
```html
<body>
  <header>
    <nav>...</nav>
  </header>
  <main>
    <h1>cheatsheets.one</h1>
  </main>
  <footer>
    <p>©2023 cheatsheets.one</p>
  </footer>
</body>
```


### Header Navigation
```html
<header>
  <nav>
    <ul>
      <li><a href="#">Edit Page</a></li>
      <li><a href="#">Twitter</a></li>
      <li><a href="#">Facebook</a></li>
    </ul>
  </nav>
</header>
```


### HTML5 Tags

|                                                                                    |                                        |
|------------------------------------------------------------------------------------|----------------------------------------|
| [article](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article)       | Content that’s independent             |
| [aside](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside)           | Secondary content                      |
| [audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)           | Embeds a sound, or an audio stream     |
| [bdi](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bdi)               | The Bidirectional Isolate element      |
| [canvas](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas)         | Draw graphics via JavaScript           |
| [data](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/data)             | Machine readable content               |
| [datalist](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist)     | A set of pre-defined options           |
| [details](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)       | Additional information                 |
| [dialog](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)         | A dialog box or sub-window             |
| [embed](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed)           | Embeds external application            |
| [figcaption](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figcaption) | A caption or legend for a figure       |
| [figure](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)         | A figure illustrated                   |
| [footer](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer)         | Footer or least important              |
| [header](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)         | Masthead or important information      |
| [main](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)             | The main content of the document       |
| [mark](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/mark)             | Text highlighted                       |
| [meter](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter)           | A scalar value within a known range    |
| [nav](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav)               | A section of navigation links          |
| [output](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output)         | The result of a calculation            |
| [picture](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)       | A container for multiple image sources |
| [progress](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress)     | The completion progress of a task      |
| [rp](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rp)                 | Provides fall-back parenthesis         |
| [rt](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/rt)                 | Defines the pronunciation of character |
| [ruby](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ruby)             | Represents a ruby annotation           |
| [section](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)       | A group in a series of related content |
| [source](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/source)         | Resources for the media elements       |
| [summary](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/summary)       | A summary for the <details> element   |
| [template](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/template)     | Defines the fragments of HTML          |
| [time](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time)             | A time or date                         |
| [track](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track)           | Text tracks for the media elements     |
| [video](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)           | Embeds video                           |
| [wbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/wbr)               | A line break opportunity               |


### HTML5 Video
```html
<video controls="" width="100%">
    <source src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.mp4" type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>
```


### HTML5 Audio
```html
<audio controls
    src="https://interactive-examples.mdn.mozilla.net/media/cc0-audio/t-rex-roar.mp3">
    Your browser does not support the audio element.
</audio>
```


### HTML5 Ruby
```html
<ruby>
  漢 <rp>(</rp><rt>かん</rt><rp>)</rp>
  字 <rp>(</rp><rt>じ</rt><rp>)</rp>
</ruby>
```


### HTML5 kdi
```html
<ul>
 <li>User <bdi>hrefs</bdi>: 60 points</li>
 <li>User <bdi>jdoe</bdi>: 80 points</li>
 <li>User <bdi>إيان</bdi>: 90 points</li>
</ul>
```


### HTML5 progress
```html
<progress value="50" max="100"></progress>
```

### HTML5 mark
```html
<p>I Love <mark>cheatsheets.one</mark></p>
```



## HTML Tables
### Table Example
```html
<table>
    <thead>
        <tr>
            <td>name</td>
            <td>age</td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Roberta</td>
            <td>39</td>
        </tr>
        <tr>
            <td>Oliver</td>
            <td>25</td>
        </tr>
    </tbody>
</table>
```



### HTML Table Tags

| Tag                                                                               | Description                      |
|-----------------------------------------------------------------------------------|----------------------------------|
| [<table>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)       | Defines a table                  |
| [<th>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th)             | Defines a header cell in a table |
| [<tr>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr)             | Defines a row in a table         |
| [<td>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td)             | Defines a cell in a table        |
| [<caption>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption)   | Defines a table caption          |
| [<colgroup>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/colgroup) | Defines a group of columns       |
| [<col>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/col)           | Defines a column within a table  |
| [<thead>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead)       | Groups the header content        |
| [<tbody>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody)       | Groups the body content          |
| [<tfoot>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tfoot)       | Groups the footer content        |

### <td> Attributes

| Attribute | Description                                   |
|-----------|-----------------------------------------------|
| `colspan` | Number of columns a cell should span          |
| `headers` | One or more header cells a cell is related to |
| `rowspan` | Number of rows a cell should span             |

See: [td\#Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attributes)



### <th> Attributes

| Attribute                                                                        | Description                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------|
| `colspan`                                                                        | Number of columns a cell should span          |
| `headers`                                                                        | One or more header cells a cell is related to |
| `rowspan`                                                                        | Number of rows a cell should span             |
| `abbr`                                                                           | Description of the cell's content             |
| [scope](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th#attr-scope) | The header element relates to                 |

See: [th Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th#attributes)



## HTML Lists
### Unordered list
```html
<ul>
    <li>I'm an item</li>
    <li>I'm another item</li>
    <li>I'm another item</li>
</ul>
```
See: [The Unordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)


### Ordered list

```html
<ol>
    <li>I'm the first item</li>
    <li>I'm the second item</li>
    <li>I'm the third item</li>
</ol>
```
See: [The Ordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)


### Definition list

```html
<dl>
    <dt>A Term</dt>
    <dd>Definition of a term</dd>
    <dt>Another Term</dt>
    <dd>Definition of another term</dd>
</dl>
```
See: [The Description List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)




## HTML Forms
### Form tags
```html
<form method="POST" action="api/login">
  <label for="mail">Email: </label>
  <input type="email" id="mail" name="mail">
  <br/>
  <label for="pw">Password: </label>
  <input type="password" id="pw" name="pw">
  <br/>
  <input type="submit" value="Login">
  <br/>
  <input type="checkbox" id="ck" name="ck">
  <label for="ck">Remember me</label>
</form>
```

The HTML `<form>` element is used to collect and send information to an external source.


### Form Attribute
| Attribute  | Description                                                                                         |
|------------|-----------------------------------------------------------------------------------------------------|
| `name`     | Name of form for scripting                                                                          |
| `action`   | URL of form script                                                                                  |
| `method`   | HTTP method, `POST` / `GET` (default)                                                             |
| `enctype`  | Media type, See [enctype](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/enctype) |
| `onsubmit` | Runs when the form was submit                                                                       |
| `onreset`  | Runs when the form was reset                                                                        |





### Label tags
```html
<!-- Nested label -->
<label>Click me 
<input type="text" id="user" name="name"/>
</label>
```
---
```html
<!-- 'for' attribute -->
<label for="user">Click me</label>
<input id="user" type="text" name="name"/>
```
`for` in a label references an input's `id` attribute





### Input tags
```html
<label for="Name">Name:</label>
<input type="text" name="Name" id="">
```

See: [HTML input Tags](/html#html-input-tags)


### Textarea tags
Textarea is a multiple-line text input control
```html
<textarea rows="2" cols="30" name="address" id="address"></textarea>
```




### Radio Buttons
Radio buttons are used to let the user select exactly one

```html
<input type="radio" name="gender" id="m">
<label for="m">Male</label>
<input type="radio" name="gender" id="f">
<label for="f">Female</label>
```




### Checkboxes
Checkboxes allows the user to select one or more

```html
<input type="checkbox" name="s" id="soc">
<label for="soc">Soccer</label>
<input type="checkbox" name="s" id="bas">
<label for="bas">Baseball</label>
```




### Select tags
A select box is a dropdown list of options

```html
<label for="city">City:</label>
<select name="city" id="city">
    <option value="1">Sydney</option>
    <option value="2">Melbourne</option>
    <option value="3">Cromwell</option>
</select>
```



### Fieldset tags
```html
<fieldset>
    <legend>Your favorite monster</legend>
    <input type="radio" id="kra" name="m">
    <label for="kraken">Kraken</label><br/>
    <input type="radio" id="sas" name="m">
    <label for="sas">Sasquatch</label>
</fieldset>
```


### Datalist tags(HTML5)
```html
<label for="b">Choose a browser: </label>
<input list="list" id="b" name="browser"/>
<datalist id="list">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Internet Explorer">
  <option value="Opera">
  <option value="Safari">
  <option value="Microsoft Edge">
</datalist>
```

### Submit and Reset Buttons
`Submit` the data to server; `Reset` to default values

```html
<form action="register.php" method="post">
  <label for="foo">Name:</label>
  <input type="text" name="name" id="foo">
  <input type="submit" value="Submit">
  <input type="reset" value="Reset">
</form>
```






## HTML input Tags
### Input Attributes
The input tag is an empty element, identifying the particular type of field information to obtain from a user.
```html
<input type="text" name="?" value="?" minlength="6"	 required />
```

----

| - |                         |                                                                                                                               |
|---|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
|   | `type="…"`              | The type of data that is being input                                                                                          |
|   | `value="…"`             | Default value                                                                                                                 |
|   | `name="…"`              | Used to describe this data in the HTTP request                                                                                |
|   | `id="…"`                | Unique identifier that other HTML elements                                                                                    |
|   | `readonly`              | Stops the user from modifying                                                                                                 |
|   | `disabled`              | Stops any interaction                                                                                                         |
|   | `checked`               | The radio or checkbox select or not                                                                                           |
|   | `required`              | Being compulsory, See [required](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/required#example)               |
|   | `placeholder="…"`       | Adds a temporary, See [::placeholder](https://developer.mozilla.org/en-US/docs/Web/CSS/::placeholder#examples)                |
|   | `autocomplete="off"`    | Disable auto completion                                                                                                       |
|   | `autocapitalize="none"` | Disable auto capitalization                                                                                                   |
|   | `inputmode="…"`         | Display a specific keyboard, See [inputmode](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/inputmode)   |
|   | `list="…"`              | The id of an associated [datalist](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist)                        |
|   | `maxlength="…"`         | Maximum number of characters                                                                                                  |
|   | `minlength="…"`         | Minimum number of characters                                                                                                  |
|   | `min="…"`               | Minimum numerical value on range & number                                                                                     |
|   | `max="…"`               | Maximum numerical value on range & number                                                                                     |
|   | `step="…"`              | How the number will increment in range & number                                                                               |
|   | `pattern="…"`           | Specifies a [Regular expression](/regex), See [pattern](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) |
|   | `autofocus`             | Be focused                                                                                                                    |
|   | `spellcheck`            | Perform spell checking                                                                                                        |
|   | `multiple`              | Whether to allow [multiple](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/multiple) values                     |
|   | `accept=""`             | Expected file type in [file](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file) upload controls            |
{.left-text}

Also see: [Attributes for the <input> element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attributes)


### Input types

|                   |                                                                                                                                          |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `type="checkbox"` | <input type="checkbox" class="border border-slate-400">                                                                                   |
| `type="radio"`    | <input type="radio" class="border border-slate-400">                                                                                      |
| `type="file"`     | <input type="file" class="border border-slate-400">                                                                                       |
| `type="hidden"`   | <input type="hidden" class="border border-slate-400">                                                                                     |
| `type="text"`     | <input type="text" class="border border-slate-400">                                                                                       |
| `type="password"` | <input type="password" class="border border-slate-400">                                                                                   |
| `type="image"`    | <input type="image" src="https://raw.githubusercontent.com/mdn/learning-area/master/html/forms/image-type-example/login.png" width="70"> |
| `type="reset"`    | <input type="reset" class="border border-slate-400">                                                                                      |
| `type="button"`   | <input type="button" class="border border-slate-400">Button</input>                                                                       |
| `type="submit"`   | <input type="submit" class="border border-slate-400">                                                                                     |

### New Input Types in HTML5
|                         |                                                                     |
|-------------------------|---------------------------------------------------------------------|
| `type="color"`          | <input type="color" value="#0FB881" class="border border-slate-400"> |
| `type="date"`           | <input type="date" class="border border-slate-400">                  |
| `type="time"`           | <input type="time" class="border border-slate-400">                  |
| `type="month"`          | <input type="month" class="border border-slate-400">                 |
| `type="datetime-local"` | <input type="datetime-local" class="border border-slate-400">        |
| `type="week"`           | <input type="week" class="border border-slate-400">                  |
| `type="email"`          | <input type="email" class="border border-slate-400">                 |
| `type="tel"`            | <input type="tel" class="border border-slate-400">                   |
| `type="url"`            | <input type="url" class="border border-slate-400">                   |
| `type="number"`         | <input type="number" class="border border-slate-400">                |
| `type="search"`         | <input type="search" class="border border-slate-400">                |
| `type="range"`          | <input type="range" class="border border-slate-400">                 |


### Input CSS selectors

|               |                           |
|---------------|---------------------------|
| `input:focus` | When its keyboard focused |
See: [Input pseudo classes](/css#input-pseudo-classes)


## HTML meta Tags
### Meta tags

The meta tag describes meta data within an HTML document. It explains additional material about the HTML.


```html
<meta charset="utf-8">
```

```html
<!-- title -->
<title>···</title>
<meta property="og:title"  content="···">
<meta name="twitter:title" content="···">
```
---

```html
<!-- url -->
<link rel="canonical"       href="https://···">
<meta property="og:url"  content="https://···">
<meta name="twitter:url" content="https://···">
```
---

```html
<!-- description -->
<meta name="description"         content="···">
<meta property="og:description"  content="···">
<meta name="twitter:description" content="···">
```
---

```html
<!-- image -->
<meta property="og:image"  content="https://···">
<meta name="twitter:image" content="https://···">
```
---

```html
<!-- ua -->
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
```
---

```html
<!-- viewport -->
<meta name="viewport" content="width=device-width">
<meta name="viewport" content="width=1024">
```




### Open Graph
Used by Facebook, Instagram, Pinterest, LinkedIn, etc.

```html
<meta property="og:type" content="website">
<meta property="og:locale" content="en_CA">
<meta property="og:title" content="HTML cheatsheet">
<meta property="og:url" content="https://cheatsheets.one/html">
<meta property="og:image" content="https://xxx.com/image.jpg">
<meta property="og:site_name" content="Name of your website">
<meta property="og:description" content="Description of this page">
```


### Twitter Cards
```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@FechinLi">
<meta name="twitter:title" content="HTML cheatsheet">
<meta name="twitter:url" content="https://cheatsheets.one/html">
<meta name="twitter:description" content="Description of this page">
<meta name="twitter:image" content="https://xxx.com/image.jpg">
```
See: [Twitter Card Documentation](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/summary)



### Geotagging
```html
<meta name="ICBM" content="45.416667,-75.7">
<meta name="geo.position" content="45.416667;-75.7">
<meta name="geo.region" content="ca-on">
<meta name="geo.placename" content="Ottawa">
```
See: [Geotagging](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)



## Useful Tips and Links
### Deprecated Tags and Attributes

Over time, HTML evolves, leading to the deprecation of certain tags and attributes as better practices emerge. Deprecated elements may not work in all browsers and are replaced with CSS or newer HTML equivalents for better functionality and standards compliance.

#### Examples of Deprecated Tags and Their Modern Equivalents

- **`<font>`**: Use CSS `font-family`, `font-size`, `color` etc., for styling text.
- **`<center>`**: Use CSS `text-align: center;` for centering elements.
- **`<marquee>`**: Achieve similar effects with CSS animations or the `scroll-behavior` property.

#### Deprecated Attributes

- **`frameborder` on `<iframe>`**: Use CSS `border: none;` to style iframes.
- **`align` in various tags**: Use CSS `text-align` for text, and `margin`, `display: flex;` or `display: grid;` for layout adjustments.

#### Importance of Using Modern Standards
Relying on deprecated tags and attributes can lead to inconsistent behavior across different browsers and devices. Transitioning to CSS for styling and layout not only adheres to current web standards but also ensures that your content is accessible and future-proof.

Certainly, here’s how you can integrate the **Performance Best Practices** into your HTML Cheat Sheet:


### Performance Best Practices

Enhance your website's loading time and overall performance with these key tips:

- **Minimize Inline Styles**: Use external CSS files for styling to improve caching and simplify maintenance.
- **Optimize Images**: Compress images and choose the correct formats to reduce file sizes while maintaining quality.
- **Simplify HTML Structure**: Avoid deeply nested HTML to decrease browser rendering times, improving both performance and code readability.

Applying these practices will lead to faster page loads and a more efficient website, providing a better user experience.



### Useful Links

1. **MDN Web Docs - HTML**: Comprehensive resource for HTML syntax and best practices.  
   [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
2. **W3C Markup Validation Service**: Tool to check the markup validity of Web documents in HTML.  
   [https://validator.w3.org/](https://validator.w3.org/)
3. **A List Apart - For People Who Make Websites**: Explores the design, development, and meaning of web content.  
   [https://alistapart.com/](https://alistapart.com/)
4. **Can I Use**: Provides up-to-date browser support tables for support of front-end web technologies.  
   [https://caniuse.com/](https://caniuse.com/)
5. **W3Schools Online Web Tutorials**: Offers tutorials and references on web development languages.  
   [https://www.w3schools.com/](https://www.w3schools.com/)
6. **Codecademy - Learn HTML**: Interactive HTML learning platform.  
    [https://www.codecademy.com/learn/learn-html](https://www.codecademy.com/learn/learn-html)
Certainly! Here's the conversion to the specified format:
7. **HTML 5 Specification**: The official specification for HTML5, providing detailed information on standards and practices.  
   [https://www.w3.org/TR/2011/WD-html5-20110405/](https://www.w3.org/TR/2011/WD-html5-20110405/)
