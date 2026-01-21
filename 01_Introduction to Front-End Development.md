# Introduction to Front-End Development








# MODULE 01 - Get strarted with web development





## Capstone project demo: Little Lemon website
You’ve just begun your coding journey on the ```Meta front-end developer program```. By the end of this program, you'll put your new skills to work by completing a real-world portfolio project, where you'll create your own dynamic ```front-end web application```. Completing this project will help you to validate the knowledge and skills that you have gained.

### What you will be able to develop
You will build this web app yourself in ```React``` and use all of the excellent tools available. Putting your newly acquired skills into practice, you will demonstrate how to build and program part of a responsive web app. 

It includes the following elements:
- A home screen with information about the restaurant.
- A table reservation system.
- A profile screen for users to enter their personal details.
- Navigation that enables users to move between parts of the web app.


**Best of luck in your coding journey.**





## Additional Resources
**Learn more**
Here is a list of resources that may be helpful as you continue your learning journey.

### What is a Web Server? (NGINX)
https://www.nginx.com/resources/glossary/web-server/

### What is a Web Browser? (Mozilla)
https://www.mozilla.org/en-US/firefox/browsers/what-is-a-browser/

### Who invented the Internet? And why? (Kurzgesagt) 
https://youtu.be/21eFwbb48sE

### What is Cloud Computing? (Amazon)
https://youtu.be/mxT233EdY5c

### Browser Engines (Wikipedia)
https://en.wikipedia.org/wiki/Browser_engine





## HTTP examples
This reading explores the contents of HTTP requests and responses in more depth.



### Request Line
Every HTTP request begins with the request line.

This consists of the HTTP method, the requested resource and the HTTP protocol version.

```HTTP
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
After the request line, the ```HTTP headers`` are followed by a line break.

There are various possibilities when including an HTTP header in the HTTP request. A header is a case-insensitive name followed by a: and then followed by a value.

Common headers are:`
```HTTP
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

```HTTP
HTTP/1.1 200 OK
```

The line begins with the HTTP protocol version, followed by the status code and a reason phrase. The reason phrase is a textual representation of the status code.



### HTTP Status Codes
The first digit of an HTTP status code indicates the category of the response: Information, Successful, Redirection, Client Error or Server Error.

The common status codes you'll encounter for each category are:


___1XX Informational___

| Status Code | Reason Phrase | Description
| -- | -- | -- |
| 100 | Continue | The server received the request headers and should continue to send the request body.
| 101 | Switching Protocols | The client has requested the server to switch protocols and the server has agreed to do so.


___2XX Successful___
| Status Code | Reason Phrase | Description |
| -- | -- | -- |
| 200 | OK | Standard response returned by the server to indicate it successfully processed the request.
| 201 | Created | The server successfully processed the request and a resource was created.
| 202 | Accepted | The server accepted the request for processing but the processing has not yet been completed.
| 204 | No Content | The server successfully processed the request but is not returning any content.


___3XX Redirection___
| Status Code | Reason Phrase | Description |
| -- | -- | -- |
| 301 | Moved Permanently | This request and all future requests should be sent to the returned location. 
| 302 | Found | This request should be sent to the returned location.


___4XX Client Error___

| Status Code | Reason Phrase | Description |
| 400 | Bad Request | The server cannot process the request due to a client error, e.g., invalid request or transmitted data is too large.
| 401 | Unauthorized | The client making the request is unauthorized and should authenticate.
| 403 | Forbidden | The request was valid but the server is refusing to process it. This is usually returned due to the client having insufficient permissions for the website, e.g., requesting an administrator action but the user is not an administrator.
| 404 | Not Found | The server did not find the requested resource.
| 405 | Method Not Allowed | The web server does not support the HTTP method used.


__5XX Server Error__

| Status Code | Reason Phrase | Description |
| 500 | Internal Server Error | A generic error status code given when an unexpected error or condition occurred while processing the request.
| 502 | Bad Gateway | The web server received an invalid response from the Application Server.
| 503 | Service Unavailable | The web server cannot process the request.



### HTTP Response Headers
Following the status line, there are optional HTTP response headers followed by a line break.

Similar to the request headers, there are many possible HTTP headers that can be included in the HTTP response.

Common response headers are:
```HTTP
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html
```

* The ```Date``` header specifies the date and time the HTTP response was generated.
* The ```Server``` header describes the web server software used to generate the response.
* The ```Content-Length``` header describes the length of the response.
* The ```Content-Type``` header describes the media type of the resource returned (e.g. HTML document, image, video).



### HTTP Response Body
Following the HTTP response headers is the ```HTTP response body```. 

This is the main content of the HTTP response. This can contain images, video, HTML documents and other media types.

```HTTP
HTTP/1.1 200 OK
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html

<html>
  <head><title>Test</title></head>
  <body>Test HTML page.</body>
</html>
```





## Other Internet Protocols
Hypertext Transfer Protocols (HTTP) are used on top of Transmission Control Protocol (TCP) to transfer webpages and other content from websites. This reading explores other protocols commonly used on the Internet.



### Dynamic Host Configuration Protocol (DHCP)
You've learned that computers need IP addresses to communicate with each other. When your computer connects to a network, the Dynamic Host Configuration Protocol or DHCP as it is commonly known, is used to assign your computer an IP address.
Your computer communicates over User Datagram Protocols (UDP) using the protocol with a type of server called a DHCP server. The server keeps track of computers on the network and their IP addresses. It will assign your computer an IP address and respond over the protocol to let it know which IP address to use. Once your computer has an IP address, it can communicate with other computers on the network.



### Domain Name System Protocol (DNS)
Your computer needs a way to know with which IP address to communicate when you visit a website in your web browser, for example, meta.com. The Domain Name System Protocol, commonly known as DNS, provides this function. Your computer then checks with the DNS server associated with the domain name and then returns the correct IP address.



### Internet Message Access Protocol (IMAP)
Do you check your emails on your mobile or tablet device? Or maybe you use an email application on your computer?
Your device needs a way to download emails and manage your mailbox on the server storing your emails. This is the purpose of the Internet Message Access Protocol or IMAP.



### Simple Mail Transfer Protocol (SMTP)
Now that your emails are on your device, you need a way to send emails. The Simple Mail Transfer Protocol, or SMTP, is used. It allows email clients to submit emails for sending via an SMTP server. You can also use it to receive emails from an email client, but IMAP is more commonly used.



### Post Office Protocol (POP)
The Post Office Protocol (POP) is an older protocol used to download emails to an email client. The main difference in using POP instead of IMAP is that POP will delete the emails on the server once they have been downloaded to your local device. Although it is no longer commonly used in email clients, developers often use it to implement email automation as it is a more straightforward protocol than IMAP.



### File Transfer Protocol (FTP)
When running your websites and web applications on the Internet, you'll need a way to transfer the files from your local computer to the server they'll run on. The standard protocol used for this is the File Transfer Protocol or FTP. FTP allows you to list, send, receive and delete files on a server. Your server must run an FTP Server and you will need an FTP Client on your local machine. You'll learn more about these in a later course.



### Secure Shell Protocol (SSH)
When you start working with servers, you'll also need a way to log in and interact with the computer remotely. The most common method of doing this is using the Secure Shell Protocol, commonly referred to as SSH. Using an SSH client allows you to connect to an SSH server running on a server to perform commands on the remote computer.
All data sent over SSH is encrypted. This means that third parties cannot understand the data transmitted. Only the sending and receiving computers can understand the data.



### Secure File Transfer Protocol (SFTP)
The data is transmitted insecurely when using the ```File Transfer Protocol (FTP)```. This means that third parties may understand the data that you are sending. This is not right if you transmit company files such as software and databases. To solve this, the ```SSH File Transfer Protocol```, alternatively called the ```Secure File Transfer Protocol (SFTP)```, can be used to transfer files over the SSH protocol. This ensures that the data is transmitted securely. Most FTP clients also support the SFTP protocol.





## Examine a web page


### Introduction
In this exercise, you will practice examining an ```HTML page``` using the developer tools.


### Goal
* Inspect the ```HTML document``` using the developer tools in your browser.


### Objectives
* Find the ```HTML ID``` of the Little Lemon logo.


### Mac OS Note:
There may be slight operational differences depending on the browser and version you use on a Mac. For instance, it varies when using **Safari** or another browser like **Chrome** or **Firefox**.


### Safari on Mac
1. Go to **Safari > Settings (or Preferences)** from the top menu bar.
2. Click on the **Advanced** tab.
3. Check the box for **"Show Develop menu in menu bar"** at the bottom.
4. Control-click (or right-click) the logo image.
5. Select **Inspect Element** from the context menu.
6. The **Web Inspecto**r will open for further inspection.


### Chrome or Firefox on Mac
1. Chrome and Firefox have developer tools enabled by default.
2. Control-click (or right-click) the logo image.
3. Select **Inspect (Chrome)** or **Inspect Element (Firefox)** from the context menu.
4. The developer tools will open for inspection.


### Mac OS summary:
- **Safari** requires enabling the **Develop menu** first (if not already enabled.)
- **Chrome** and **Firefox** come with inspection tools enabled by default.


### Instructions
1. **Step 1:** Download the following file on your local system.

[examine_the_page.zip][page101]

2. **Step 2:** Unzip the file (Windows)

On Windows, open your Downloads folder, right-click the file examine_the_page.zip and select Extract All.

![Display for Unzipping to Select Destination and Extract Files][img101]

2. **Step 2:** Unzip the file (Mac)

On Mac, open your Downloads folder and double click the file examine_the_page.zip.

Once unzipped, there will be a folder named examine_the_page.

3. **Step 3:**  Open the folder and double click index.html to view the file in your local web browser. Verify that it looks similar to the image below. 

**Tip:** The page adapts to different screen sizes. Its appearance changes depending on the device you're using and the size of your browser window.

![Little Lemon Our Menu Webpage preview][img102]


4. **Step 4:**  

Windows: Right-click the Little Lemon logo and select Inspect (or Inspect Element)

Mac:  Control-click the logo image and select Inspect (or Inspect Element)  

![Right Click Display on the Page][img103]

5. **Step 5:** Inspect the line in the HTML for the logo in the developer tools panel. The line begins with ```<img```.

**Note:** In the line, there is an ID in the following format id="???". Note the value that the ID is equal to.

![Inspect code for img tag][img104]
![Inspect code for  id value inside img tag][img105]


### Tips
* If you get stuck, close the developer tools and start over.
* Review the lesson Developer Tools.


### OS Note:
There may be slight operational differences depending on the browser and version you use on a Mac. For instance, it varies when using Safari or another browser like Chrome or Firefox.


### Safari on Mac
1. Go to Safari > Settings (or Preferences) from the top menu bar.
2. Click on the Advanced tab.
3. Check the box for "Show Develop menu in menu bar" at the bottom.
4. Control-click (or right-click) the logo image.
5. Select Inspect Element from the context menu.
6. The Web Inspector will open for further inspection.


### Chrome or Firefox on Mac
1. Chrome and Firefox have developer tools enabled by default.
2. Control-click (or right-click) the logo image.
3. Select **Inspect (Chrome)** or **Inspect Element (Firefox)** from the context menu.
4. The developer tools will open for inspection.


### In summary:
- **Safari** requires enabling the **Develop menu** first (if not already enabled.)
- **Chrome** and **Firefox** come with inspection tools enabled by default.





## Exercise: Edit a website using a browser developer tools


### Introduction
In this exercise, you will practice editing an HTML page using the developer tools.

### Goal
- Edit the HTML document using the developer tools in your browser.


### Objectives
- Change the text of Our Menu to Little Lemon Menu.

### Instructions
- **Step 1:** Download the following file on your local system.

_Note: If you have completed the exercise Examine the Page, you can skip steps 1 and 2 as the file contains the same assets from that exercise._

[examine-the-page][page101]

- **Step 2:** Unzip the file.
<u>On Windows</u>, open your Downloads folder, right-click the file examine_the_page.zip and select Extract All.

![Display for Unzipping to Select Destination and Extract Files][img106]
 
On Mac, open your Downloads folder or the default location for your Downloads. The file might automatically unzip, but double-click and unzip it manually if needed. It should create a folder named 'examine_the_page' and locate the file index.html inside.

- **Step 3:**  Open the index.html file in your local browser for preview. Verify that it looks like this:

![Little Lemon Our Menu Webpage preview][img107]

- **Step 4:** Right-click the Our Menu text and select Inspect or Inspect Element.

![Display for right click on Menu][img108]

- **Step 5:** Double-click the Our Menu text in the Elements tab of the developer tools panel.

- **Step 6:** Change the text to Little Lemon Menu.

- **Step 7:** Close the developer tools.

- **Step 8:** Verify that the text has changed on the web page.

### Tips
- If you get stuck, close the developer tools and start from the beginning.
- Review the lesson Developer Tools.





## Setting up your local development environment
This reading walks you through the steps to set up an Integrated Development Environment, or IDE, on a Windows and on a Mac (further down below).

The IDE you'll be using in the course is ```Visual Studio Code```, which Microsoft provides for free and comes with a wealth of plugins and extensions to make your life as a developer easier.

You have two options for using Visual Studio Code to complete your course activities:

**Option 1: Use Visual Studio Code in-browser with Coursera Labs**

Coursera’s platform offers an in-browser version of Visual Studio Code which is preconfigured and requires no local setup. You can access the Visual Studio Code environment through the “Lab” items included in this course. Your work and files will be saved and available within this in-browser lab while you have course access.

**Option 2: Work on your local device**

You can also choose to complete your work on your local machine if you prefer. This will require a few steps of set up in advance. 

First, you need to download the IDE from Microsoft's website - https://code.visualstudio.com/download.

Select the download based on your operating system.


### Windows
1. **Step 1:** Download the Windows installer.
2. **Step 2:** Open the file to install it once the download is complete.
3. **Step 3:** Review and accept the license agreement, then click Next.
![Set up Visual Studio Code on Microsoft Step 3][img109]

4. **Step 4:** Keep the default value when prompted for the destination location and click next.
![Set up Microsoft Visual Studio Code Step 4][img110]

5. **Step 5:** On the additional tasks view, make sure that Add to PATH is selected. 
![Set up Microsoft Visual Studio Code Step 5 ][img111]

6. **Step 6:** Click next.
7. **Step 7:** Click install when the ready to install page appears.
![Set up Microsoft Visual Studio Code Step 7][img112]

8. **Step 8:** Click finish once completed, and the application will launch.


### Mac
1. Step 1: Download the application based on the chipset you have. M1 macs use Apple Silicon, and older Macs use Intel. If you are not sure, choose the Universal option.
2. Step 2: Go to your Downloads folder once the download is complete. 
3. Step 3: Double-click the zip file to extract the contents.
4. Step 4: Drag and drop the .app file to the application link in Finder below.
![Set up Visual Studio Code on Mac Step 4][img113]

5. Step 5: Open the app.

### Linux

Please refer to the official [Linux installation guide](https://code.visualstudio.com/docs/setup/linux) for Visual Studio Code.

### Selecting a working directory
Now that you have Visual Studio Code set up create a folder on your device that you'll use to do course exercises.

Open Visual Studio Code, go to File and select Open Folder. Using the file browser, select the folder you just created.

Congratulations, you're set up now to begin writing some code.





## Visual Studio Code on Coursera
In addition to having Visual Studio Code installed on your own computer, in this course and throughout this program, you'll have the opportunity to work in Visual Studio Code right here on Coursera!   

As you progress through the course, you'll be able to write code in hands-on activities called **Labs**. In these labs you'll be able to open Visual Studio Code and start writing code without ever leaving the course.

You'll have plenty of opportunities to see Labs in action later in the course, but for now, use the images below as a visual guide to how Labs will look and operate in your browser.

**Note:** This guide uses screenshots to show you where to find important buttons, menus, and other controls. However, you can't click or interact with the images in this reading. They are here to alert you to the location and use of commands to prepare you for the actual lab exercises.

![Lab][img114]

The Labs contain instructions explaining the coding task.

![Creating an HTML Document][img115]

Please note that the image above is for demonstration of how the lab will appear for you. When you click the button **Open Lab** in the actual lab, a new tab will open with Visual Studio Code already setup and ready for you to start writing code! 

![Open Lab][img116]

You'll see all the files for the lab in the Project folder in the left sidebar.

![Files][img117]

And the large editor area where you write your code for the lab.

![Terminal][img118]

You may need to use a tool called the Terminal from time to time to complete course activities. You can open this by selecting the **Terminal** option in the upper Visual Studio Code toolbar.

![Terminal 2][img119]


### How to download files from your Visual Studio Code Lab to your local device

1. Select the Lab Files button in your Lab Toolbar. 

2. You'll be able to download your full workspace, specific folders, or individual files through the checkbox selection tool. 

3. After you've selected these files, use the **Download** link to download your files to your local device. 

![How to upload local files to your Visual Studio Code Lab][img120]


### How to upload local files to your Visual Studio Code Lab
If you'd like to upload your course files from your local device to your Visual Studio Code lab, drag and drop your file from your local device into the Visual Studio Code file tree.

![How to upload local files to your Visual Studio Code Lab][img121]

### How to get a fresh copy of course-provided starter files
Your work will be saved and persist within your Visual Studio Code lab while you are enrolled in the course. If you'd like to get a fresh copy of the original instructor-provided files at any time, you can do this through the **Lab Help** option in your Lab Toolbar.  Don't worry - your original work and files will still remain in your lab until you personally remove or delete them, even when refreshing your files through the steps below.

1. First rename your original files to something like [yourfilename] [original].[your file extension]`. You can do this by right-clicking on your file in the Visual Studio Code file tree, selecting **Rename**, and providing a new file name.

- For example for index.html, this could be renamed to `index [original].html`

2. Select **Lab Help** from your Lab Toolbar and then select **Get latest version**. 

![Lab Help][img122]

3. You should now see a fresh copy of the original instructor-provided files in your lab, in addition to your own  (renamed) files.





## Additional Resources
### Learn more
Here is a list of resources that may be helpful as you continue your learning journey.

### HTTP Overview (Mozilla)
https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview

### Introduction to Networking by Dr.Charles R Severance
https://www.amazon.com/Introduction-Networking-How-Internet-Works/dp/1511654945/

### Chrome Developer Tools Overview (Google)
https://developer.chrome.com/docs/devtools/overview/

### Firefox Developer Tools User Docs  (Mozilla)
https://firefox-source-docs.mozilla.org/devtools-user/index.html

### Getting Started with Visual Studio Code  (Microsoft)
https://code.visualstudio.com/docs










# MODULE 02 - Introduction to HTML and CSS





## Simple HTML tags
There are many tags available in ```HTML```. Here you will learn about common tags that you'll use as a developer.


### Headings
Headings allow you to display titles and subtitles on your webpage.

```HTML
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

![Heading style displayed in browser][img010201]



### Paragraphs
Paragraphs contain text content.

```HTML
<p>
   This paragraph
   contains a lot of lines
   but they are ignored.
</p>
```

The following displays in the web browser: 

![Paragraph style displayed in browser ][img010202]

**Note** that putting content on a new line is ignored by the web browser.



### Line Breaks
As you've learned, line breaks in the paragraph tag line are ignored by HTML. Instead, they must be specified using the ```<br>``` tag. The ```<br>``` tag does not need a closing tag.

```HTML
<p>
   This paragraph<br>
   contains a lot of lines<br>
   and they are displayed.
</p>
```

The following displays in the web browser: 

![Line breaks displayed in browser][img010203]



### Strong
Strong tags can be used to indicate that a range of text has importance.

```HTML
<p>
   No matter how much the dog barks: <strong>don't feed him chocolate</strong>.
</p>
```

The following displays in the web browser: 

![Text with strong tag displayed in browser][img010204]



### Bold
Bold tags can be used to draw the reader's attention to a range of text.

```HTML
<p>
   The primary colors are <b>red</b>, <b>yellow</b> and <b>blue</b>.
</p>
```

The following displays in the web browser: 

![Bold text displayed in browser][img010205]

The following displays in the web browser: 

![Text with strong tag displayed in browser][img010206]

Bold tags should be used to draw attention but not to indicate that something is more important. Consider the following example:

```HTML
The three core technologies of the Internet are <b>HTML</b>, <b>CSS</b> and <b>Javascript</b>.
```

The following displays in the web browser: 

![Bold text displayed in browser][img010207]



### Emphasis
Emphasis tags can be used to add emphasis to text.

```HTML
<p>
   Wake up <em>now</em>!
</p>
```

The following displays in the web browser: 

![Text with emphasis tag displayed in browser][img010208]



### Italics
Italics tags can be used to offset a range of text.

```
<p>
   The term <i>HTML</i> stands for HyperText Markup Language.
</p>
```

The following displays in the web browser: 

![Italic text displayed in browser][img010209]



### Emphasis vs. Italics
By default both tags will have the same visual effect in the web browser. The only difference is the meaning.

Emphasis tags stress the text contained in them. Let's explore the following example:

```HTML
I <em>really</em> want ice cream.
```

The following displays in the web browser: 

![Text with emphasis tag displayed in browser.][img010210] 

Italics represent off-set text and should be used for technical terms, titles, a thought or a phrase from another language, for example:

```HTML
My favourite book is <i>Dracula</i>.
```

The following displays in the web browser: 

![Italic text displayed in browser][img010211]

Screen readers will not announce any difference if an italics tag is used.



### Lists
You can add lists to your web pages. There are two types of lists in ```HTML```.

Lists can be unordered using the ```<ul>``` tag. List items are specified using the ```<li>``` tag, for example:

```HTML
<ul>
   <li>Tea</li>
   <li>Sugar</li>
   <li>Milk</li>
</ul>
```

This displays in the web browser as:

![Bullet style displayed in the browser img10][img010212]

Lists can also be ordered using the ```<ol>``` tag. Again, list items are specified using the ```<li>``` tag.

```HTML
<ol>
   <li>Rocky</li>
   <li>Rocky II</li>
   <li>Rocky III</li>
</ol>
```

This displays as the following in the web browser.

![Numbered list style displayed in browser img11][img010213]



### Div tags
A ```<div>``` tag defines a content division in a ```HTML``` document. It acts as a generic container and has no effect on the content unless it is styled by ```CSS```.

The following example shows a ```<div>``` element that contains a paragraph element:

```HTML
<div>
   <p>This is a paragraph inside a div</p>
</div>
```

This displays as the following in the web browser.

![Div displayed in browser img12][img010214]

It can be nested inside other elements, for example:

```HTML
<div>
   <div>
      <p>This is a paragraph inside a div that’s inside another div</p>
   </div>
</div>
```

This displays in the web browser as:

![Div inside a dive displayed in browser][img010215]

As mentioned, the ```div``` has no impact on content unless it is styled by ```CSS```. Let’s add a small ```CSS``` rule that styles all divs on the page.

Don't worry about the meaning of the ```CSS``` just yet, you'll explore ```CSS``` further in a later lesson. In summary, you're applying a rule that adds a border and some visual spacing to the element.

```HTML
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
```

This displays in the web browser as:

![Paragraph in stylized div displayed in browser img13][img010216]

```Div``` elements are an important part of building webpages. More advanced usage of div elements will be explored in another course.



### Comments
If you want to leave a comment in the code for other developers, it can be added as:

```HTML
<!-- This is a comment --> 
```

The comment will not be displayed in the web browser.





## Additional Resources
### Learn more
Here is a list of resources that may be helpful as you continue your learning journey.

### HTML Elements Reference (Mozilla)
https://developer.mozilla.org/en-US/docs/Web/HTML/Element

### The Form Element (Mozilla)
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form

### What is the Document Object Model? (W3C)
https://www.w3.org/TR/WD-DOM/introduction.html

### ARIA in HTML (W3C via Github)
https://w3c.github.io/html-aria/

### ARIA Authoring Practices  (W3C)
https://www.w3.org/TR/wai-aria-practices-1.2/





## Different types of selectors
When styling a web page, there are many types of selectors available that allow developers to be as broad or as specific as they need to be when selecting HTML elements to apply CSS rules to.

Here you will learn about some of the common CSS selectors that you will use as a developer.


### Element Selectors
The element selector allows developers to select HTML elements based on their element type.

For example, if you use ```p``` as the selector, the rule will apply to all ```p``` elements on the webpage.

#### HTML

```HTML
<p>Once upon a time...</p>
<p>In a hidden land...</p>
```
#### CSS

```CSS
p { 
  color: blue; 
}
```


### ID Selectors
The ID selector uses the id attribute of an HTML element. Since the id is unique within a webpage, it allows the developer to select a specific element for styling. ID selectors are prefixed with a ```#``` character.

#### HTML
```HTML
<span id="latest">New!</span>
```

#### CSS
```CSS
#latest { 
  background-color: purple; 
}
```


### Class Selectors
Elements can also be selected based on the class attribute applied to them. The CSS rule has been applied to all elements with the specified class name. The class selector is prefixed with a ```.``` character.

In the following example, the CSS rule applies to both elements as they have the ```navigation``` CSS class applied to them.

#### HTML
```HTML
<a class="navigation">Go Back</a>
<p class="navigation">Go Forward</p>
```

```CSS
.navigation { 
  margin: 2px;
}
```


### Element with Class Selector
A more specific method for selecting HTML elements is by first selecting the HTML element, then selecting the CSS class or ID.

The example below selects all p elements that have the CSS class introduction applied to them.

#### HTML
```HTML
<p class="introduction"></p>
```

#### CSS
```CSS
p.introduction { 
  margin: 2px;
}
```


### Descendant Selectors
Descendant selectors are useful if you need to select HTML elements that are contained within another selector.

Let's explore an example.

You have the following HTML structure and CSS rule.

#### HTML

```HTML
<div id="blog">
  <h1>Latest News</h1>
  <div>
    <h1>Today's Weather</h1>
    <p>The weather will be sunny</p>
  </div>
  <p>Subscribe for more news</p>
</div>
<div>
  <h1>Archives</h1>
</div>
```

#### CSS
```CSS
#blog h1 {
  color: blue;
}
```

The CSS rule will select all ```h1``` elements that are contained within the element with the ID ```blog```. The CSS rule will not apply to the ```h1``` element containing the text ```Archives```.

The structure of a descendant selector is a CSS selector, followed by a single space character, followed by another CSS selector.

Multiple descendants can also be selected. For example, to select all h1 elements that are descendants of ```div``` elements which are descendants of the ```blog``` element, the selector is specified as follows.

#### CSS
```CSS
#blog div h1 {
  color: blue;
}
```


### Child Selectors
Child selectors are more specific than descendant selectors. They only select elements that are immediate descendants (children) of a selector (the parent).

For example, you have the following HTML structure:

#### HTML

```HTML
<div id="blog">
  <h1>Latest News</h1>
  <div>
    <h1>Today's Weather</h1>
    <p>The weather will be sunny</p>
  </div>
  <p>Subscribe for more news</p>
</div>
```

If you wanted to style the h1 element containing the text Latest News, you can use the following child selector:

#### CSS
```CSS
#blog > h1 {
  color: blue;
}
```

This will select the element with the ID ```blog``` (the parent), then it will select all ```h1``` elements that are contained directly in that element (the children). The structure of the child selector is a CSS selector followed by the child combinator symbol > followed by another CSS selector.

**Note** that this will not go beyond a single depth level. Therefore, the CSS rule will **not** be applied to the ```h1``` element containing the text ```Today's Weather```.

### :hover Pseudo-Class
A special keyword called a pseudo-class allows developers to select elements based on their state. Don't worry too much about what that means right now. For now, let's look at how the hover pseudo-class allows you to style an element when the mouse cursor hovers over the element.

The simplest example of this is changing the color of a hyperlink when it is hovered over. To do this, you add the ```:hover``` pseudo-class to the end of the selector. In the following example, adding ```:hover```  to the a element will change the color of the hyperlink to orange when it is hovered over.

#### CSS
```CSS
a:hover {
  color: orange;
}
```

This pseudo-class is very useful for creating visual effects based on user interaction.

### Other Selectors
There are many other CSS selectors available to style your webpage. 





## Text and color in CSS
As you design websites, you'll be working a lot with colors and text. There are many different ways to display text and equally as many ways to define colors.

This reading covers how text and color work in CSS.


### Color
Colors are used in many CSS properties, for example:

```CSS
p { 
  color: blue; 
}
```

From CSS Version 3, there are five main ways to reference a color.
- By RGB value,
- By RGBA value,
- By HSL value,
- By hex value and
- By predefined color names.


### RGB value
RGB is a color model that adds the colors ```red (R)```, ```green (G)``` and ```blue (B)``` together to create colors. This is based on how the human eye sees colors.

Each value is defined as a number between ```0``` and ```255```, representing the intensity of that color.

For example, the color **RED** would have the RGB value of ```255,0,0``` since the intensity of the red color would be 100% while blue and green would be 0%.

The color **BLACK** then would be ```0,0,0``` and the color **WHITE** ```255,255,255```.

When using RGB values in CSS, they can be defined using the ```rgb``` keyword:

```CSS
p { 
  color: rgb(255, 0, 0); 
}
```


### RGBA value
RGBA is an extension of RGB that add an ```alpha (A)``` channel. The alpha channel represents the ```opacity```, or transparency, of the color.

Similar to RGB, this is specified in CSS using the rgba keyword:

```CSS
p { 
  color: rgba(255, 0, 0, 0.8); 
}
```


### HSL value
```HSL``` is a newer color model defined as ```Hue (H)```, ```Saturation (S)``` and ```Lightness (L)```. The aim of the model is to simplify mental visualization of the color that the value represents.

Think of a rainbow that has been turned into a full circle. This represents the Hue. The Hue value is the degree value on this circle, from 0 degrees to 360 degrees. ```0``` is **RED**, ```120``` is **GREEN** and ```240``` is **BLUE**.

![Color gradient palette displaying Hue and Saturation][img010217]

Saturation is the distance from the center of the circle to its edge. The saturation value is represented by a percentage from 0% to 100% where ```0%``` is the **center** of the circle and ```100%``` is its **edge**. For example, 0% will mean that the color is more grey and 100% represents the full color.

Lightness is the third element of this color model. Think of it as turning the circle into a 3D cylinder where the bottom of the cylinder is more black and toward the top is more white. Therefore, lightness is the distance from the bottom of the cylinder to the top. Again, lightness is represented by a percentage from 0% to 100% where 0% is the bottom of the cylinder and 100% is its top. In other words, 0% will mean that the color is more black and 100% is white.

![Color Diagram for Hue, Saturation and Lightness][img010218]

In CSS, you use the ```hsl``` keyword to define a color with HSL.

```CSS
p { 
  color: hsl(0, 100%, 50%);
}
```


### Hex value

Colors can be specified using a hexadecimal value. If you're unfamiliar with hexadecimal, think of it as a different number set.

Decimal is what you use every day. Digits range from 0 to 9 before tens and hundreds are used.

Hexadecimal is similar, except it has 16 digits. This is counted as ```0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F.```

In fact, you can convert between decimal and hexadecimal. Decimal 10 is equal to hexadecimal ```A```. Hexadecimal ```F``` is equal to decimal ```15```.

Hexadecimal can also go to tens and hundreds. For example, decimal 16 is equal to hexadecimal 10, with 10 being the next number after F.

It can be a little confusing at first but don't worry, there are plenty of converters available if you get stuck.

Colors specified using hexadecimal are prefixed with a # symbol followed by the RGB value in hexadecimal format.

For example, the color red which is RGB 255,0,0 would be written as hexadecimal #FF0000.

Again don't worry if you get stuck, there are plenty of converters available for this too!


### Predefined color names
Modern web browsers support 140 predefined color names. These color names are for convenience purposes and can be mapped to equivalent hex/RGB/HSL values.

Some common color names available are listed below.

```HTML
black
silver
gray
white
maroon
red
purple
fuchsia
green
lime
olive
yellow
navy
blue
teal
aqua
```


### Text
With CSS there are many ways to change how text is displayed. In this section, you'll learn the most common text manipulation CSS properties.



### Text Color
The ```color``` property sets the color of text. The following CSS sets the text color for all paragraph elements to red.

```CSS
p { 
  color: red;
}
```


### Text Font and Size
There are many different fonts to display text on your computer. In simple terms, a font is a collection of text characters written in a specific style and size.

If you've used a word processor before, you're probably familiar with the fonts Times New Roman and Calibri.

To set the font used by text in CSS you use the ```font-family``` property.

```CSS
p { 
  font-family: "Courier New", monospace;
}
```

Since computers vary in what fonts they have installed, it is recommended to include several fonts when using the ```font-family``` property. These are specified in a fallback order, meaning that if the first font is not available, it will check for the second font. If the second font is not available, then it will check for the third font and so on. If none of the fonts are available, it will use the browser's default font.

To set the size of the font, the ```font-size``` property is used.

```CSS
p { 
  font-family: "Courier New", monospace;
  font-size: 12px;
}
```



### Text Transformation
Text transformation is useful if you want to ensure the correct capitalization of the text content. In the example below, the CSS rule will change all text in paragraph elements to uppercase using the ```text-transform``` property:

```CSS
p { 
  text-transform: uppercase;
}
```

The most commonly used values for the ```text-transform``` property are:  ```uppercase```,  ```lowercase```,  ```capitalize```  and  ```none```. The default value used is none, which means the text displays as it was written in the HTML document.



### Text Decoration
The ```text-decoration``` property is useful to apply additional decoration to text such as underlining and line-through (strikethrough).

```CSS
p { 
  text-decoration: underline;
}
```

It is possible to set the color, thickness and styling of the decoration too. In the example below, the underline will be a solid red line that is 5 pixels thick.

```CSS
p { 
  text-decoration: underline red solid 5px;
}
```

If this is confusing, don't worry. These properties can be individually set using the ```text-decoration-line```, ```text-decoration-color```, ```text-decoration-style``` and ```text-decoration-thickness``` properties. Let's use the same example again and define it using the individual properties:

```CSS
p { 
  text-decoration-line: underline;
  text-decoration-color: red;
  text-decoration-style: solid;
  text-decoration-thickness: 5px;
}
```

The most common ```text-decoration-line``` values used are: ```underline```, ```overline```, ```line-through``` and ```none```. None is the default value to use no text decoration.

There are many styles available for the ```text-decoration-style```  property;  ```solid```,  ```double```,  ```dotted```,  ```dashed```  and  ```wavy```. The text-decoration-style property requires the decoration line to be defined. If the decoration style is not specified, ```solid``` will be used.





## Alignment basics
Let's explore how to align text and HTML elements using CSS.

Let's first focus on horizontal alignment. Vertical alignment is more difficult so you'll explore that later on.

### Text Alignment

Aligning text within an HTML element is very simple. To do this, you use the ```text-align``` CSS property. In the following example, the CSS rule is setting the text of all paragraph elements to be center aligned.

```CSS
p {
    text-align: center;
}
```
Text alignment can be set to ```left``` , ```right```, ```center``` and ```justify```.

The ```justify``` alignment spreads the text out so that every line of the text has the same width.

The default alignment is ```left``` for languages that are left-to-right such as English. For right-to-left languages such as Arabic, the default alignment is ```right```.



### HTML Element Alignment
HTML element alignment is more complicated than text alignment. To align HTML elements, you must consider the box model and document flow from previous lessons. Aligning an HTML element is done by changing the properties of its box model and how it impacts the document flow.

### HTML Element Center Alignment
To center align an element, you set a width on the element and push its margins out to fill the remaining available space of the parent element as in the following HTML structure:

```HTML
<div class="parent">
  <div class="child">
  </div>
</div>
```

In your CSS, you'll set the ```parent``` element to have a red border to visualize the space it occupies:

```CSS
.parent {
  border: 4px solid red;
}
```

The ```child``` element will have a width equal to 50% of the ```parent``` element with a padding of 20 pixels. Note that ```padding: 20px``` is shorthand for setting the padding top, bottom, left and right to ```20px```. To visualize the space it occupies, set the border to green:

```CSS
.child {
  width: 50%;
  padding: 20px;
  border: 4px solid green;
}
```

To align the element to the center, set its ```margin``` property to ```auto```. The ```auto``` will tell the browser to calculate the margin automatically based on the space available.

```CSS
.child {
  width: 50%;
  padding: 20px;
  border: 4px solid green;
  margin: auto;
}
```

The result is the ```child``` element is centered within the ```parent``` element:

![Alignment of the child in the parent element][img010219]

It is important to note that this works because the div element is a block-level element.  

If you want to align an inline element like img, you will need to change it to a block-level element. Similar to the div example, you add the img to a parent element:

```HTML
<div class="parent">
  <img src="photo.png" class="child">
</div>
```

The CSS rule then changes the ```img``` element to a block-level element and sets its margin to ```auto```:

```CSS
.child {
  display: block;
  width: 50%;
  margin: auto;
}
```

To be more precise, in CSS you can set only the left and right margins to auto. This allows you to set the top and bottom margins to specific values if needed.

```CSS
.child {
  display: block;
  width: 50%;
  margin-left: auto;
  margin-right: auto;
}
```



### HTML Element Left / Right Alignment
The two most common ways to left and right align elements are to use the float property and the ```position``` property.

The ```position``` property has several value options that impact how the element displays in the document flow. You'll explore how to use the position property later on. For now, let's focus on the ```float``` property.

The ```float``` property sets an element's position relative to the text content within a parent element. Text will wrap around the element.

In the following example, the image will be aligned to the right of the div element. The text content will wrap around the image:

#### HTML
```HTML
<div class="parent">
  <img src="photo.png" class="child"> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur eu odio eget leo auctor porta sit amet sit amet justo. Donec fermentum quam in diam volutpat, at lacinia diam placerat. Aenean quis feugiat sem. Suspendisse a dui massa. Phasellus scelerisque, mi vestibulum iaculis tristique, orci tellus gravida nisi, in pellentesque elit massa ut lorem. Sed elementum ornare nunc vel cursus. Duis sed enim in nulla efficitur convallis sed eget dolor. Curabitur scelerisque eros erat, in vulputate dolor consequat vel. Praesent ac sapien condimentum, ultricies libero at, auctor orci. Curabitur ut augue ac massa convallis faucibus sed in magna. Phasellus scelerisque auctor est a auctor. Nam laoreet sem sapien, porta imperdiet urna laoreet eu. Morbi dolor turpis, congue id bibendum eget, viverra et risus. Quisque vitae erat id tortor ullamcorper maximus.
</div>
```

#### CSS
```CSS
.child {
  float: right;
}
```

The following displays in the web browser:  

![Text displayed in browser that is right-aligned using the float property][img010220]





## Additional resources

### Learn more
Here is a list of resources that may be helpful as you continue your learning journey.

### CSS Reference (Mozilla)
https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

### HTML and CSS: Design and build websites by Jon Duckett
https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/

### CSS Definitive Guide  by Eric Meyer  
https://www.amazon.com/CSS-Definitive-Guide-Visual-Presentation/dp/1449393195/









# MODULE 03 - UI Frameworks





## Bootstrap
Bootstrap is often described as a way to "build fast, responsive sites" and it is a "feature-packed, powerful, and extensible frontend toolkit". 

Some people refer to it as a "front-end" framework, and some are trying to be more specific by referring to it as a "CSS framework" or a “CSS library”. 

So, what is Bootstrap?

Simply put, Bootstrap is a library of CSS and JavaScript code that you can combine to quickly build visually appealing websites.

Modern web development is all about **components**. Small pieces of reusable code that allow you to build websites quickly. Bootstrap comes with multiple components for very fast construction of multiple components, or parts of components. 

Another important aspect of modern development is **responsive grids** which allow web pages to adapt their layout and content depending on the device in which they are viewed. Bootstrap comes with a pre-made set of CSS rules for building a responsive grid.

Bootstrap is very popular amongst developers as it saves development time and provides a way for developers to build visually appealing prototypes and websites.

Bootstrap saves significant time because all the CSS code that styles its grid and pre-built components is already written. Instead of needing a high level of expertise in various CSS concepts, you can simply use the existing Bootstrap CSS classes to create visually appealing websites. This is indispensable when you need to quickly iterate on website layouts.

Once you know how Bootstrap works, you’ll have enough knowledge to tweak its styling and a whole new world of development opens up to you.

Since Bootstrap is so popular, understanding how to work with it is a prerequisite in many web development companies. Additionally, you can be safe in knowing that both you and your team members have a common design system and you don't have to spend time deciding how to build one. You are free to jump from team to team, from project to project, even from one company to another, and you don't need to re-learn "their way of doing things".

All of these points make investing time to learn Bootstrap a great way to boost your web development skills. In this lesson, you’ll be introduced to the core concepts of Bootstrap and learn how to build web pages using it.





## Using Bootstrap documentation
Bootstrap comes with detailed documentation on setting up and using the features available in its library. The documentation is clear and has many code examples to help you get started.

In this reading, you'll explore the frequently used documentation sections.

The documentation for Bootstrap is currently available at the following link.

https://getbootstrap.com/docs

### Navigating the documentation
The sidebar on the webpage allows you to navigate through the different sections of the documentation. There is also a search box if you need to search for a specific piece of information.

![Using the sidebar in the Bootstrap documentation][img010301]



### Layout
The layout section of the documentation describes how to use the grid system of Bootstrap. This covers what you've learned so far and includes more advanced usage such as offsets, column alignment, auto-layout and variable width columns.

![Layout section of the Bootstrap documentation][img010302]



### Content
The content section of the documentation describes Bootstrap's default text styling and how to use responsive images and tables. You've learned the basics of these earlier on and this section goes into further detail.

![The content section of the Bootstrap documentation][img010303]



### Forms
The forms section of the documentation describes how to build forms using Bootstrap's styles. The library has many CSS rules to improve your form's user interface and experience. Below are some features you'll frequently use as a developer:

![The Forms section of the Bootstrap documentation][img010304]

#### Form Styling
Bootstrap includes CSS rules to improve the visual style of input elements.

For example:

![Bootstrap Form Styling][img010305]

This table outlines the different HTML form elements and which Bootstrap CSS class should be used for them.

| Form Element | CSS class |
| -- | -- |
| input | form-control |
| input type="checkbox" | form-check-input | 
| input type="radio" | form-check-input |
| input type="range" | form-range |
| select | form-select | 

Using these CSS classes will style the elements appropriately for different input types, sizings and states. More information is available on the [Forms documentation page](https://getbootstrap.com/docs/5.0/forms/overview/).



### Switches
If you've used an app on your mobile device, you're probably familiar with the switch input type.

![Bootstrap Doc Switches][img010306]

Bootstrap includes CSS rules to style checkbox input elements as switches. 

To do this:
1. Add the input to a div element. 
2. On the div element, apply the form-check and form-switch CSS classes. 
3. On the input element, add the form-check-input CSS class.

```HTML
<div class="form-check form-switch">
  <input class="form-check-input" type="checkbox">
</div>
```

More information is available in the [Switches section of the documentation](https://getbootstrap.com/docs/5.0/forms/checks-radios/#switches).




### Input Groups
Input groups are useful for providing additional content to the input field. For example, if you wanted to request the user to input a US dollar amount, you can use an input group to show the dollar symbol and cents amount.

![Bootstrap Input Groups][img010307]

To do this:
1. Add the input to a div element. 
2. Apply the input-group CSS classes on the div element. 
3. Add a ```span``` element before and/or after the input element and apply the ```input-group-text``` CSS class to it. The text content is then added inside the ```span``` element.

```HTML
<div class="input-group">
  <span class="input-group-text">$</span>
  <input type="text" class="form-control">
  <span class="input-group-text">.00</span>
</div>
```

More information is available on the [Input Groups documentation page](https://getbootstrap.com/docs/5.0/forms/input-group/).




### Floating Labels
Floating labels help provide form information to the user as part of the input itself. These are different from regular form placeholders. The information stays visible if the user is interacting with the element or if the element has content.

![Bootstrap floating label][img010308]

![Bootstrap floating label][img010309]

To do this, add the ```input``` to a ```div``` element. On the ```div``` element, apply the ```form-floating``` CSS classes.

```HTML
<div class="form-floating">
  <input type="email" class="form-control" id="addressInput" placeholder="Address">
  <label for="addressInput">Address</label>
</div>
```

More information is available on the [Floating Labels documentation page](https://getbootstrap.com/docs/5.0/forms/floating-labels/)




### Components
As you have learned, Bootstrap comes with many pre-made UI elements and styles to help speed up your development.

Some of these components require Javascript to work, while others only require CSS classes applied to HTML elements. The Components section of the documentation explains these requirements on each component page and provides many code examples.

![The components section of the Bootstrap documentation][img010310]



### Conclusion
Now that you are familiar with how to use the Bootstrap documentation, maybe try some new components and styles on a webpage that you've previously built.





## Other CSS frameworks and libraries
As a developer, you'll use many CSS libraries and frameworks throughout your career. As you move on to different projects and as technologies advance, knowing what solutions are available is critical. While Bootstrap is one of the most popular CSS libraries, many others are available, each with different purposes, designs and technical approaches. This reading will introduce you to other popular CSS libraries and frameworks.

Foundation
Official Website

Foundation is a framework for building user interfaces similar to Bootstrap. It is used by many large companies such as Pixar, Polar and Sonos. One prominent feature of Foundation is that it can be used to style content for sending via email.

CSS frameworks: Foundation website
Pure.css
Official Website

Pure.css is another library for building user interfaces. While it doesn't have as many features as Bootstrap, it is designed to be minimal in file size. Smaller file sizes improve loading times for web pages as there is less data to transfer from the web server. If your next project is focused on minimal loading time, this library is worth considering.

CSS frameworks: Pure website 
Tailwind CSS
Official Website

Tailwind CSS is a CSS framework that uses a utility-based approach for its CSS rules. This means that the framework provides many CSS classes with a single purpose. For example, the CSS class pt-6 sets the padding-top CSS property to 6 pixels. This means that you can be precise in applying styling to your HTML without writing CSS. The advantage to this is that it is more flexible for customizing your webpage's design using the framework. However, the disadvantage is that if multiple developers are working on a project, it could lead to inconsistent design if the team is not strict on its design rules.

CSS frameworks: Tailwindcss website
UIKit
Official Website

UIKit is a lightweight CSS framework featuring a small set of responsive components. Its simple design allows developers to easily customize the style rules and visuals.

CSS frameworks: UIKit website
MVP.css
Official Website

MVP.css is a small CSS library that automatically styles HTML elements without needing to apply CSS classes to them. The library aims to allow a developer to quickly prototype a user interface without worrying about the final design, while still being visually appealing. MVP comes from the technical term Minimal Viable Product, a product with sufficient features to demo to customers or other business stakeholders.

CSS frameworks: MVP.css website
Conclusion
If you're curious to learn more about these frameworks, their websites feature set up guides, tutorials and documentation to get started. It is a good exercise to compare and contrast different libraries and frameworks to understand different workflows available to you as a developer.






## Additional Resources
Bootstrap Official Website

https://getbootstrap.com/

Bootstrap 5 Foundations by Daniel Foreman  

https://www.amazon.com/Bootstrap-Foundations-Mr-Daniel-Foreman/dp/B0948GRS8W/

Responsive Web Design with HTML5 and CSS  by Ben Frain  

https://www.amazon.com/Responsive-Web-Design-HTML5-CSS/dp/1839211563/

Bootstrap Themes  

https://themes.getbootstrap.com/





## Case Study: Why did Facebook engineers create React?
There are a lot of JavaScript Model-View-Controller (MVC) frameworks out there. Why did we build React and why would you want to use it?

React isn’t an MVC framework.
React is a library for building composable user interfaces. It encourages the creation of reusable UI components which present data that changes over time.

React doesn’t use templates.
Traditionally, web application UIs are built using templates or HTML directives. These templates dictate the full set of abstractions that you are allowed to use to build your UI.

React approaches building user interfaces differently by breaking them into components. This means React uses a real, full-featured programming language to render views, which we see as an advantage over templates for a few reasons:

JavaScript is a flexible, powerful programming language with the ability to build abstractions. This is incredibly important in large applications.

By unifying your markup with its corresponding view logic, React can actually make views easier to extend and maintain.

By baking an understanding of markup and content into JavaScript, there’s no manual string concatenation and therefore less surface area for XSS vulnerabilities.

We’ve also created 
JSX
, an optional syntax extension, in case you prefer the readability of HTML to raw JavaScript.

React updates are dead simple.
React really shines when your data changes over time.

In a traditional JavaScript application, you need to look at what data changed and imperatively make changes to the DOM to keep it up-to-date. Even AngularJS, which provides a declarative interface via directives and data binding 
requires a linking function to manually update DOM nodes
.

React takes a different approach.

When your component is first initialized, the render method is called, generating a lightweight representation of your view. From that representation, a string of markup is produced and injected into the document. When your data changes, the render method is called again. In order to perform updates as efficiently as possible, we diff the return value from the previous call to render with the new one and generate a minimal set of changes to be applied to the DOM.

The data returned from render is neither a string nor a DOM node — it’s a lightweight description of what the DOM should look like.

We call this process reconciliation. Check out 
this jsFiddle
 to see an example of reconciliation in action.

Because this re-render is so fast (around 1ms for TodoMVC), the developer doesn’t need to explicitly specify data bindings. We’ve found this approach makes it easier to build apps.

HTML is just the beginning.
Because React has its own lightweight representation of the document, we can do some pretty cool things with it:

Facebook has dynamic charts that render to <canvas> instead of HTML.

Instagram is a “single page” web app built entirely with React and Backbone.Router. Designers regularly contribute React code with JSX.

We’ve built internal prototypes that run React apps in a web worker and use React to drive native iOS views via an Objective-C bridge.

You can run React on the server for SEO, performance, code sharing and overall flexibility.

Events behave in a consistent, standards-compliant way in all browsers (including IE8) and automatically use event delegation.

Head on over to 
https://reactjs.org
 to check out what we have built.





 ## The Virtual DOM
React builds a representation of the browser Document Object Model or DOM in memory called the virtual DOM. As components are updated, React checks to see if the component’s HTML code in the virtual DOM matches the browser DOM. If a change is required, the browser DOM is updated. If nothing has changed, then no update is performed.

As you know, this is called the reconciliation process and can be broken down into the following steps:

Step 1: The virtual DOM is updated.

Step 2: The virtual DOM is compared to the previous version of the virtual DOM and checks which elements have changed.

Step 3: The changed elements are updated in the browser DOM.

Step 4: The displayed webpage updates to match the browser DOM.

As updating the browser DOM can be a slow operation, this process helps to reduce the number of updates to the browser DOM by only updating when it is necessary.

But even with this process, if a lot of elements are updated by an event, pushing the update to the browser DOM can still be expensive and cause slow performance in the web application.

The React team invested many years of research into solving this problem. The outcome of that research is what’s known as the React Fiber Architecture.

The Fiber Architecture allows React to incrementally render the web page. What this means is that instead of immediately updating the browser DOM with all virtual DOM changes, React can spread the update over time. But what does "over time" mean?

Imagine a really long web page in the web browser. If the user scrolls to the bottom, the top of the web page is no longer visible. The user then clicks a button on the bottom of the web page that updates some text on the top of the web page.

But the top of the page isn’t visible. Therefore, why update it immediately?

Perhaps there is text currently displayed on the bottom of the page that also updates when the button is clicked. Wouldn’t that be a higher priority to update than the non-visible text?

This is the principle of the React Fiber Architecture. React can optimize when and where updates occur to the browser DOM to significantly improve application performance and responsiveness to user input. Think of it as a priority system. The highest priority changes, the elements visible to the user, are updated first. While lower priority changes, the elements not currently displayed, are updated later.

While you’re unlikely to interact with the virtual DOM and Fiber Architecture yourself, it’s good to know what’s going on if issues occur during the development of your web application.

There are many tools available to help you investigate how React is processing your webpage. The official React Developer Tools web browser plugin developed by Meta will be one of the key tools in your developer toolbox. So, if you do have to look deeper into the code, you’ll have the right toolbox available to help you. These tools will be explored later on. 






## Alternatives to React
React is a library and not a framework. This means you'll often use other JavaScript libraries with it to build your application. In this reading, you will be briefly introduced to some JavaScript libraries commonly used with React.

Lodash
Official Website

As a developer, there's a lot of logic you'll commonly write across applications. For example, you might need to sort a list of items or round a number such as 3.14 to 3. Lodash provides common logic such as these as a utility library to save you time as a developer.

Other Javascript libraries: Lodash
Luxon
Official Website

You'll be working with dates and times often as a developer. Think of viewing a list of orders and when they were placed, or displaying a calendar schedule for an event. Dates and times are everywhere.

Luxon helps you work with dates and times by providing functions to manipulate and display them. For example, think of how dates are formatted in different countries. In the United States the format is Month Day Year but in Europe it is Day Month Year. This is one area where Luxon can help you display the date in the user's local format.

Other Javascript libraries: Luxon
Redux
Official Website

When building a web application, you'll need to keep track of its state. Think of when you shop online. The web application tracks items currently in your shopping cart. When you remove an item from the cart, the application needs to update what displays on the screen. This is where Redux comes in. It helps you manage your application state and even has advanced features such as undo and redo.

Other Javascript libraries: Redux
Axios
Official Website

As a developer you'll be communicating with APIs over HTTP frequently. The Axios library helps to simplify sending HTTP requests and processing the response. It also provides advanced features allowing you to cancel requests and to change data received from the web server before your application uses the data.

Other Javascript libraries: Axios 
Jest
Official Website

It is good practice to write automated tests for your code as a professional developer. The jest library helps you to do this and works with many libraries and frameworks. It also provides reporting utilities such as providing information on how much of your code is tested by your automated tests.

Other Javascript libraries: Jest 
Conclusion
If you're curious to learn more about these libraries, their websites feature setup guides, tutorials and documentation to get started. These libraries will be covered later on.






## Additional Resources
Learn more
Here is a list of resources that may be helpful as you continue your learning journey.

React Official Website
https://reactjs.org/

Choosing between Traditional Web Apps and Single Page Apps (Microsoft)

https://docs.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/choose-between-traditional-web-and-single-page-apps

React Source Code (Github)

https://github.com/facebook/react

Introduction to React.js  

The original video recorded at Facebook in 2013.

https://youtu.be/XxVg_s8xAms






# MODULE 04







# Public

[img101]: /front-end-development/public/images/101_windows_unzip.png
[img102]: /front-end-development/public/images/102_Examine-Web-Page.jpeg
[img103]: /front-end-development/public/images/103_little_lemon_logo_right_click.png
[img104]: /front-end-development/public/images/104_examine_page_inspect_logo_id.png
[img105]: /front-end-development/public/images/105_examine_page_inspect_logo_id.png
[img106]: /front-end-development/public/images/106_windows_unzip.png
[img107]: /front-end-development/public/images/107_Examine-Web-Page.jpeg
[img108]: /front-end-development/public/images/108_little_lemon_menu_right_click.png
[img109]: /front-end-development/public/images/109_vscode_license.png
[img110]: /front-end-development/public/images/110_vscode_install_location.png
[img111]: /front-end-development/public/images/111_path_selected.png
[img112]: /front-end-development/public/images/112_vscode_ready_to_install.png
[img113]: /front-end-development/public/images/113_mac_install_app.png
[img114]: /front-end-development/public/images/114_Screen-Shot-2022-06-24-at-3.39.41-PM.png
[img115]: /front-end-development/public/images/115_Screen-Shot-2022-06-24-at-12.54.48-PM.png
[img116]: /front-end-development/public/images/116_Screen-Shot-2022-06-24-at-3.42.35-PM.png
[img117]: /front-end-development/public/images/117_files.png
[img118]: /front-end-development/public/images/118_editor.png
[img119]: /front-end-development/public/images/119_VSCode-Terminal-Example.png
[img120]: /front-end-development/public/images/120_Lab-VSCode-File-Download.png
[img121]: /front-end-development/public/images/121_VSCode-File-Upload.png
[img122]: /front-end-development/public/images/122_Refresh-Lab-Files.png

[img010201]: /front-end-development/public/images/img010201_html_headings.png
[img010202]: /front-end-development/public/images/img010202_html_paragraph.png
[img010203]: /front-end-development/public/images/img010203_html_line_breaks.png
[img010204]: /front-end-development/public/images/img010204_html_strong.png
[img010205]: /front-end-development/public/images/img010205_html_bold.png
[img010206]: /front-end-development/public/images/img010206_html_strong2.png
[img010207]: /front-end-development/public/images/img010207_html_bold2.png
[img010208]: /front-end-development/public/images/img010208_html_italics.png
[img010209]: /front-end-development/public/images/img010209_html_italics.png
[img010210]: /front-end-development/public/images/img010210_html_emphasis2.png
[img010211]: /front-end-development/public/images/img010211_html_italics2.png
[img010212]: /front-end-development/public/images/img010212_html_unordered_list.png
[img010213]: /front-end-development/public/images/img010213_html_ordered_list.png
[img010214]: /front-end-development/public/images/img010214_html_div_no_style.png
[img010215]: /front-end-development/public/images/img010215_html_nested_div.png
[img010216]: /front-end-development/public/images/img010216_html_nested_div_with_style.png
[img010217]: /front-end-development/public/images/img010217_text_color_hue.png
[img010218]: /front-end-development/public/images/img010218_text_color_hue2.png
[img010219]: /front-end-development/public/images/img010219_css_center_div.png
[img010220]: /front-end-development/public/images/img010220_css_float_right.png

[img010301]: /front-end-development/public/images/img010301_bootstrap_docs_navigation.png
[img010302]: /front-end-development/public/images/img010302_bootstrap_docs_layout.png
[img010303]: /front-end-development/public/images/img010303_bootstrap_docs_content.png
[img010304]: /front-end-development/public/images/img010304_bootstrap_docs_forms.png
[img010305]: /front-end-development/public/images/img010305_bootstrap_form_control.png
[img010306]: /front-end-development/public/images/img010306_bootstrap_docs_switches.png
[img010307]: /front-end-development/public/images/img010307_bootstrap_input_group.png
[img010308]: /front-end-development/public/images/img010308_bootstrap_docs_floating_label1.png
[img010309]: /front-end-development/public/images/img010309_bootstrap_docs_floating_label2.png
[img010310]: /front-end-development/public/images/img010310_bootstrap_docs_components.png

[page101]: /front-end-development/01_Introduction%20to%20Front-End%20Development/examine_the_page/index.html


[img201]:/front-end-development/public/images/01_bootstrap_docs_navigation.png
[img202]:/front-end-development/public/images/02_bootstrap_docs_layout.png
[img203]:/front-end-development/public/images/03_bootstrap_docs_content.png
[img204]:/front-end-development/public/images/04_bootstrap_docs_forms.png
[img205]:/front-end-development/public/images/05_bootstrap_form_control.png
[img206]:/front-end-development/public/images/06_bootstrap_docs_switches.png
[img207]:/front-end-development/public/images/07_bootstrap_input_group.png
[img208]:/front-end-development/public/images/08_bootstrap_docs_floating_label1.png
[img209]:/front-end-development/public/images/09_bootstrap_docs_components.png