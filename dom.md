# DOM Intro

---
<!--Slide 2-->
# Objectives

1. Explain what the DOM is.
2. Describe the relationship between the DOM and HTML.
3. Explain what the document is.
4. Explore and interact with the DOM using browser dev tools.

---
<!--Slide 3-->

> What is your understanding of the DOM?
-- Think, Pair, Share

---


# The DOM is ...


1. a programming interface (API) for HTML (and XML) documents. 
1. a fully object-oriented representation of the web page.
1. can be modified with a scripting language such as JavaScript.

---


# What is an API?

1. Application Programming Interface:
A system that allows you to access the features of something

---


# The DOM is an object

HTML is a document.
The DOM is an object that represents the HTML.
HTML tags become elements within the DOM.

---


# The Document

1. A document can be textually represented via HTML (how the developer sees a web page).
1. A document can be visually represented via the browser window (how the user sees a web page).
1. A document can be digitally represented via the DOM (how the program sees a webpage).


---


# Activity 1

1. With a partner:
2. You Do #1

---


# Activity 2

1. By yourself:
2. You Do #2

---


# The DOM is a tree.

1. Root
2. Nodes

![](http://cdn.mos.cms.futurecdn.net/4cd370bb2f7a7c3394da687bf6ca07b7.jpg)

---


# Check for Understanding

```html
<html>
  <head>
    <title>Some Title</title>
  </head>

  <body>
    <h1>Some Header</h1>
    <div>
      <p>text inside p inside div</p>
    </div>
  </body>
</html>
```

---

<!--Slide -->
# Objectives

1. Explain what the DOM is.
2. Describe the relationship between the DOM and HTML.
3. Explain what the document is.
4. Explore and interact with the DOM using browser dev tools.

---


# The DOM is...


1. The Document Object Model (DOM) is a programming interface (API) for HTML (and XML) documents. 
1. a fully object-oriented representation of the web page.
1. can be modified with a scripting language such as JavaScript.

---


# The Document

1. A document can be textually represented via HTML (how the developer sees a web page).
1. A document can be visually represented via the browser window (how the user sees a web page).
1. A document can be digitally represented via the DOM (how the program sees a webpage).


---

# DOM Traversal

---

# Objectives for Traversing the DOM

1. Query the the DOM for nodes using CSS selectors.
2. Traverse the DOM using parent, sibling and children nodes.
3. Access the values of HTML attributes and the innerText of a node.

---

# Querying the DOM

1. Methods
2. Outputs
	- Elements vs Nodes
	- HTML Collections
	- NodeLists

---



# Object Methods for Querying the DOM

getElementbyID
getElementsByClassName
getElementsByName
getElementsByTagName
getElementsByTagNameNS
querySelector
querySelectorAll

---


# Activity

Two whiteboards

1. Divide into groups of four
	- Consult the documents for your DOM method
	- Consider your inputs and outputs
2. On two whiteboards
	- clarify inputs and outputs
	- On another white board, write example code

---

# Activity

Group 1: getElementbyID
Group 2: getElementsByClassName
Group 3: getElementsByName
Group 4: getElementsByTagName
Group 5: getElementsByTagNameNS
Group 6: querySelector
Group 7: querySelectorAll

---


# Traversing the DOM

1. Methods
2. Outputs


---


# Object Methods for Traversing the DOM

childNodes
firstChild
lastChild
parentNode
nextSibling
previousSibling

---

# Accessing values in the DOM

1. HTML attributes
2. innerText

---


# Objectives for Traversing the DOM

1. Query the the DOM for nodes using CSS selectors.
2. Traverse the DOM using parent, sibling and children nodes.
3. Access the values of HTML attributes and the innerText of a node.

---

# DOM Manipulation

---

# Objectives for Manipulating the DOM

1. Set an element’s text.
2. Add, update, and remove styles on elements.
3. Add, update, and remove classes on elements.
4. Add, update, and remove attributes on elements.
5. Create and access data-attributes on elements.

---

# Changing an element’s value
1. Open up google.com
2. In the browser console, query the DOM for the “Google Search” button.
3. Change the “value” property to 'Ask Jeeves';

---

## Possible Solution

document.querySelector
('input[name="btnK"]').value = “Ask Jeeves”

---

# Setting an element's text
1. Query the Advertising button on the bottom left.
2. Update the innerText property to “Hello innerText!”

##Bonus: What is the difference between “innerText” and “innerHTML”? (Check out the docs...)

——

## Possible Solution

document.querySelector
('#fsl > a:nth-child(1)').innerText = “Hello innerText!”

---

# Changing an element’s style
1. Open up google.com
2. Query the DOM for the “viewport” div.
3. set the style property’s backgroundColor to black.
4. What happens when you refresh the page?

——

## Possible Solution

document.getElementById
('viewport').style.backgroundColor = “black”

---

#Manipulating classes

1. Navigate to MDN's "Document Object Model" page.
2. Query the DOM for the div with the class of 'oauth-login-container'
3. Console all a list of all of the class for this div. What type of data is returned?
4. Create a new class for this div, and then check to make sure you were successful.


——

#Manipulating attributes

2. Query the DOM for the div with an id of 'wiki-document-head'
3. Remove this id attribute from the div.
4. List the attributes for the div. Did the previous step work?
5. Now, add that attribute back!

——

#Manipulating data-attributes

1. What exactly is a data-attribute? (Use the docs!)
2. Query the DOM for the span with a data-attribute of 'data-service'
3. Console all data attributes for this particular span.
4. Create a new data-attribute for the span.


——

<!-- If time -->
##Finish DOM Manipulation exercises on learn page.

---

# Objectives for Manipulating the DOM

1. Set an element’s text.
2. Add, update, and remove styles on elements.
3. Add, update, and remove classes on elements.
4. Add, update, and remove attributes on elements.
5. Create and access data-attributes on elements.

---

# DOM Creation & Deletion

---

# Objectives for Traversing the DOM

1. Create brand new DOM elements
1. Manipulate DOM elements in-memory
1. Move an existing DOM element
1. Remove elements from the DOM

---

# Creating & manipulating
document.createElement()
.appendChild()

var newSection = document.createElement('section');
newSection.innerHTML = "This is a new section."
document.body.appendChild(newSection);

---


# Moving

.replaceChild(newChild, oldChild)

var updatedSection = document.createElement('Section');
updatedSection.innerHTML = "This is a different section.";

document.body.replaceChild(updatedSection, newSection);

---


# Removal

.removeChild(child)

var nav = document.getElementById('nav');
document.body.removeChild(nav);

---

# Objectives for Traversing the DOM

1. Create brand new DOM elements
1. Manipulate DOM elements in-memory
1. Move an existing DOM element
1. Remove elements from the DOM

---