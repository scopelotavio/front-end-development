# Introduction to Front-End Development






# Module 01 - Get strarted with web development

## HTTP examples
This reading explores the contents of HTTP requests and responses in more depth.

### Request Line
Every HTTP request begins with the request line.

This consists of the HTTP method, the requested resource and the HTTP protocol version.

```http
GET /home.html HTTP/1.1
``` 

In this example, ```GET``` is the HTTP method, ```/home.html``` is the resource requested and ```HTTP 1.1``` is the protocol used.

### HTTP Methods
HTTP methods indicate the action that the client wishes to perform on the web server resource.

Common HTTP methods are:

| HTTP Method | Description
| -- | -- |
| GET | The client requests a resource on the web server. |
| POST | The client submits data to a resource on the web server.
| PUT | The client replaces a resource on the web server.
| DELETE | The client deletes a resource on the web server.
| PATCH | The client partially updates a resource on the web server.

### HTTP Request Headers
After the request line, the HTTP headers are followed by a line break.

There are various possibilities when including an HTTP header in the HTTP request. A header is a case-insensitive name followed by a: and then followed by a value.

Common headers are:
```http
Host: example.com
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: */*
Accept-Language: en
Content-type: text/json
```

* The ```Host``` header specifies the host of the server and indicates where the resource is requested from.

* The ```User-Agent``` header informs the web server of the application that is making the request. It often includes the operating system (Windows, Mac, Linux), version and application vendor.

* The ```Accept``` header informs the web server what type of content the client will accept as the response.

* The ```Accept-Language``` header indicates the language and optionally the locale that the client prefers.

* The ```Content-type``` header indicates the type of content being transmitted in the request body.

### HTTP Request Body
HTTP requests can optionally include a request body. A request body is often included when using the HTTP POST and PUT methods to transmit data.

```HTTP
POST /users HTTP/1.1
Host: example.com

{
 "key1":"value1",
 "key2":"value2",
 "array1":["value3","value4"]
}
```

```HTTP
PUT /users/1 HTTP/1.1
Host: example.com
Content-type: text/json

{"key1":"value1"}
```

### HTTP Responses
When the web server is finished processing the HTTP request, it will send back an HTTP response.

The first line of the response is the status line. This line shows the client if the request was successful or if an error occurred.

```HTTP/1.1 200 OK```

The line begins with the HTTP protocol version, followed by the status code and a reason phrase. The reason phrase is a textual representation of the status code.

### HTTP Status Codes
The first digit of an HTTP status code indicates the category of the response: Information, Successful, Redirection, Client Error or Server Error.

The common status codes you'll encounter for each category are:

_1XX Informational_ 

| Status Code | Reason Phrase | Description
| -- | -- | -- |
| 100 | Continue | The server received the request headers and should continue to send the request body.
| 101 | Switching Protocols | The client has requested the server to switch protocols and the server has agreed to do so.

_2XX Successful_
| Status Code | Reason Phrase | Description |
| -- | -- | -- |
| 200 | OK | Standard response returned by the server to indicate it successfully processed the request.
| 201 | Created | The server successfully processed the request and a resource was created.
| 202 | Accepted | The server accepted the request for processing but the processing has not yet been completed.
| 204 | No Content | The server successfully processed the request but is not returning any content.

_3XX Redirection_
| Status Code | Reason Phrase | Description |
| -- | -- | -- |
| 301 | Moved Permanently | This request and all future requests should be sent to the returned location. 
| 302 | Found | This request should be sent to the returned location.

_4XX Client Error_

| Status Code | Reason Phrase | Description |
| 400 | Bad Request | The server cannot process the request due to a client error, e.g., invalid request or transmitted data is too large.
| 401 | Unauthorized | The client making the request is unauthorized and should authenticate.
| 403 | Forbidden | The request was valid but the server is refusing to process it. This is usually returned due to the client having insufficient permissions for the website, e.g., requesting an administrator action but the user is not an administrator.
| 404 | Not Found | The server did not find the requested resource.
| 405 | Method Not Allowed | The web server does not support the HTTP method used.

_5XX Server Error_

| Status Code | Reason Phrase | Description |
| 500 | Internal Server Error | A generic error status code given when an unexpected error or condition occurred while processing the request.
| 502 | Bad Gateway | The web server received an invalid response from the Application Server.
| 503 | Service Unavailable | The web server cannot process the request.

### HTTP Response Headers
Following the status line, there are optional HTTP response headers followed by a line break.

Similar to the request headers, there are many possible HTTP headers that can be included in the HTTP response.

Common response headers are:

1234
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html
The Date header specifies the date and time the HTTP response was generated.

The Server header describes the web server software used to generate the response.

The Content-Length header describes the length of the response.

The Content-Type header describes the media type of the resource returned (e.g. HTML document, image, video).

HTTP Response Body
Following the HTTP response headers is the HTTP response body. This is the main content of the HTTP response.

This can contain images, video, HTML documents and other media types.

12345678910






















# Module 02 - Introduction to HTML and CSS

## Simple HTML tags
There are many tags available in HTML. Here you will learn about common tags that you'll use as a developer.



### Headings
Headings allow you to display titles and subtitles on your webpage.

```html
<body>
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>
</body>
```

The following displays in the web browser:

![Heading style displayed in browser][img101]



### Paragraphs
Paragraphs contain text content.

```html
<p>
   This paragraph
   contains a lot of lines
   but they are ignored.
</p>
```

The following displays in the web browser: 

![Paragraph style displayed in browser][img102]

**Note** that putting content on a new line is ignored by the web browser.



### Line Breaks
As you've learned, line breaks in the paragraph tag line are ignored by HTML. Instead, they must be specified using the ```<br>``` tag. The ```<br>``` tag does not need a closing tag.

```html
<p>
   This paragraph<br>
   contains a lot of lines<br>
   and they are displayed.
</p>
```

The following displays in the web browser: 

![Line breaks displayed in browser][img103] 



### Strong
Strong tags can be used to indicate that a range of text has importance.

```html
<p>
   No matter how much the dog barks: <strong>don't feed him chocolate</strong>.
</p>
```

The following displays in the web browser: 

![Text with strong tag displayed in browser][img104]



### Bold
Bold tags can be used to draw the reader's attention to a range of text.

```html
<p>
   The primary colors are <b>red</b>, <b>yellow</b> and <b>blue</b>.
</p>
```

The following displays in the web browser: 

![Bold text displayed in browser][img105]

The following displays in the web browser: 

![Text with strong tag displayed in browser][img106]

Bold tags should be used to draw attention but not to indicate that something is more important. Consider the following example:

```html
The three core technologies of the Internet are <b>HTML</b>, <b>CSS</b> and <b>Javascript</b>.
```

The following displays in the web browser: 

![Bold text displayed in browser][img107]



### Emphasis
Emphasis tags can be used to add emphasis to text.

```html
<p>
   Wake up <em>now</em>!
</p>
```

The following displays in the web browser: 

![Text with emphasis tag displayed in browser][img108] 



### Italics
Italics tags can be used to offset a range of text.

```html
<p>
   The term <i>HTML</i> stands for HyperText Markup Language.
</p>
```

The following displays in the web browser: 

![Italic text displayed in browser][img109] 



### Emphasis vs. Italics
By default both tags will have the same visual effect in the web browser. The only difference is the meaning.

Emphasis tags stress the text contained in them. Let's explore the following example:

```html
I <em>really</em> want ice cream.
```

The following displays in the web browser: 

![Text with emphasis tag displayed in browser.][img110]

Italics represent off-set text and should be used for technical terms, titles, a thought or a phrase from another language, for example:

```html
My favourite book is <i>Dracula</i>.
```

The following displays in the web browser: 

![Italic text displayed in browser][img111]

Screen readers will not announce any difference if an italics tag is used.



### Lists
You can add lists to your web pages. There are two types of lists in HTML.

Lists can be unordered using the ```<ul>``` tag. List items are specified using the ```<li>``` tag, for example:

```html
<ul>
   <li>Tea</li>
   <li>Sugar</li>
   <li>Milk</li>
</ul>
```

This displays in the web browser as:

![Bullet style displayed in the browser][img112]

Lists can also be ordered using the ```<ol>``` tag. Again, list items are specified using the ```<li>``` tag.

```html
<ol>
   <li>Rocky</li>
   <li>Rocky II</li>
   <li>Rocky III</li>
</ol>
```

This displays as the following in the web browser.

Numbered list style displayed in browser img11
Div tags
A <div> tag defines a content division in a HTML document. It acts as a generic container and has no effect on the content unless it is styled by CSS.

The following example shows a <div> element that contains a paragraph element:

123
<div>
   <p>This is a paragraph inside a div</p>
</div>
This displays as the following in the web browser.

Div displayed in browser img12
It can be nested inside other elements, for example:

5
<div>
   <div>
      <p>This is a paragraph inside a div that’s inside another div</p>
   </div>
</div>
This displays in the web browser as:

Div inside a dive displayed in browser 
As mentioned, the div has no impact on content unless it is styled by CSS. Let’s add a small CSS rule that styles all divs on the page.

Don't worry about the meaning of the CSS just yet, you'll explore CSS further in a later lesson. In summary, you're applying a rule that adds a border and some visual spacing to the element.

1234567891011
<style>
   div {
      border: 1px solid black;
      padding: 2px;
   }
</style>
<div>
   <div>
      <p>This is a paragraph inside stylized divs</p>
   </div>

This displays in the web browser as:

Paragraph in stylized div displayed in browser img13
Div elements are an important part of building webpages. More advanced usage of div elements will be explored in another course.

Comments
If you want to leave a comment in the code for other developers, it can be added as:

<!-- This is a comment --> 

The comment will not be displayed in the web browser.

# Module 03 - UI Frameworks

## Bootstrap
Bootstrap is often described as a way to "build fast, responsive sites" and it is a "feature-packed, powerful, and extensible frontend toolkit". 

Some people refer to it as a "front-end" framework, and some are trying to be more specific by referring to it as a "CSS framework" or a “CSS library”. 

### So, what is Bootstrap?

Simply put, ```Bootstrap``` is a library of ```CSS``` and ```JavaScript``` code that you can combine to quickly build visually appealing websites.

Modern web development is all about components. Small pieces of reusable code that allow you to build websites quickly. Bootstrap comes with multiple components for very fast construction of multiple components, or parts of components. 

Another important aspect of modern development is responsive grids which allow web pages to adapt their layout and content depending on the device in which they are viewed. ```Bootstrap``` comes with a pre-made set of CSS rules for building a responsive grid.

Bootstrap is very popular amongst developers as it saves development time and provides a way for developers to build visually appealing prototypes and websites.

Bootstrap saves significant time because all the CSS code that styles its grid and pre-built components is already written. Instead of needing a high level of expertise in various CSS concepts, you can simply use the existing Bootstrap CSS classes to create visually appealing websites. This is indispensable when you need to quickly iterate on website layouts.

Once you know how Bootstrap works, you’ll have enough knowledge to tweak its styling and a whole new world of development opens up to you.

Since Bootstrap is so popular, understanding how to work with it is a prerequisite in many web development companies. Additionally, you can be safe in knowing that both you and your team members have a common design system and you don't have to spend time deciding how to build one. You are free to jump from team to team, from project to project, even from one company to another, and you don't need to re-learn "their way of doing things".

All of these points make investing time to learn Bootstrap a great way to boost your web development skills. In this lesson, you’ll be introduced to the core concepts of Bootstrap and learn how to build web pages using it.

## Using Bootstrap documentation
```Bootstrap``` comes with detailed documentation on setting up and using the features available in its library. The documentation is clear and has many code examples to help you get started.

In this reading, you'll explore the frequently used documentation sections.

The documentation for Bootstrap is currently available at the following link.

https://getbootstrap.com/docs

### Navigating the documentation
The sidebar on the webpage allows you to navigate through the different sections of the documentation. There is also a search box if you need to search for a specific piece of information.

![Using the sidebar in the Bootstrap documentation][img01]

### Layout
The layout section of the documentation describes how to use the grid system of Bootstrap. This covers what you've learned so far and includes more advanced usage such as offsets, column alignment, auto-layout and variable width columns.

Layout section of the Bootstrap documentation 
Content
The content section of the documentation describes Bootstrap's default text styling and how to use responsive images and tables. You've learned the basics of these earlier on and this section goes into further detail.

The content section of the Bootstrap documentation
Forms
The forms section of the documentation describes how to build forms using Bootstrap's styles. The library has many CSS rules to improve your form's user interface and experience. Below are some features you'll frequently use as a developer:

The Forms section of the Bootstrap documentation
Form Styling
Bootstrap includes CSS rules to improve the visual style of input elements.

For example:

Bootstrap Form Styling
This table outlines the different HTML form elements and which Bootstrap CSS class should be used for them.

Form Element

CSS class

input

form-control

input type="checkbox"

form-check-input

input type="radio"

form-check-input

input type="range"

form-range

select

form-select

Using these CSS classes will style the elements appropriately for different input types, sizings and states. More information is available on the 
Forms documentation page
.

Switches
If you've used an app on your mobile device, you're probably familiar with the switch input type.

Bootstrap Doc Switches
Bootstrap includes CSS rules to style checkbox input elements as switches. 

To do this:

Add the input to a div element. 

On the div element, apply the form-check and form-switch CSS classes. 

On the input element, add the form-check-input CSS class.

123
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox">
</div>
More information is available in the 
Switches section of the documentation
.

Input Groups
Input groups are useful for providing additional content to the input field. For example, if you wanted to request the user to input a US dollar amount, you can use an input group to show the dollar symbol and cents amount.

Bootstrap Input Groups 
To do this:

Add the input to a div element. 

Apply the input-group CSS classes on the div element. 

Add a span element before and/or after the input element and apply the input-group-text CSS class to it. The text content is then added inside the span element.

12345
<div class="input-group">
  <span class="input-group-text">$</span>
  <input type="text" class="form-control">
  <span class="input-group-text">.00</span>
</div>
More information is available on the 
Input Groups documentation page
.

Floating Labels
Floating labels help provide form information to the user as part of the input itself. These are different from regular form placeholders. The information stays visible if the user is interacting with the element or if the element has content.

Bootstrap floating label
Bootstrap floating label
To do this, add the input to a div element. On the div element, apply the form-floating CSS classes.

1234
<div class="form-floating">
  <input type="email" class="form-control" id="addressInput" placeholder="Address">
  <label for="addressInput">Address</label>
</div>
More information is available on the 
Floating Labels documentation page

Components
As you have learned, Bootstrap comes with many pre-made UI elements and styles to help speed up your development.

Some of these components require Javascript to work, while others only require CSS classes applied to HTML elements. The Components section of the documentation explains these requirements on each component page and provides many code examples.

The components section of the Bootstrap documentation
Conclusion
Now that you are familiar with how to use the Bootstrap documentation, maybe try some new components and styles on a webpage that you've previously built.

# Module 04







# Public

[img101]:/front-end-development/public/images/101_html_headings.png
[img102]:/front-end-development/public/images/102_html_paragraph.png
[img103]:/front-end-development/public/images/103_html_line_breaks.png
[img104]:/front-end-development/public/images/104_html_strong.png
[img105]:/front-end-development/public/images/105_html_bold.png
[img106]:/front-end-development/public/images/106_html_strong2.png
[img107]:/front-end-development/public/images/107_html_bold2.png
[img108]:/front-end-development/public/images/108_html_emphasis.png
[img109]:/front-end-development/public/images/109_html_italics.png
[img110]:/front-end-development/public/images/110_html_emphasis2.png
[img111]:/front-end-development/public/images/111_html_italics2.png
[img112]:/front-end-development/public/images/112_html_unordered_list.png

[img201]:/front-end-development/public/images/01_bootstrap_docs_navigation.png
[img202]:/front-end-development/public/images/02_bootstrap_docs_layout.png
[img203]:/front-end-development/public/images/03_bootstrap_docs_content.png
[img204]:/front-end-development/public/images/04_bootstrap_docs_forms.png
[img205]:/front-end-development/public/images/05_bootstrap_form_control.png
[img206]:/front-end-development/public/images/06_bootstrap_docs_switches.png
[img207]:/front-end-development/public/images/07_bootstrap_input_group.png
[img208]:/front-end-development/public/images/08_bootstrap_docs_floating_label1.png
[img209]:/front-end-development/public/images/09_bootstrap_docs_components.png