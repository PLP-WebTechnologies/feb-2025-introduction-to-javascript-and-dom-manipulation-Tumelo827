# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript DOM Interaction</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
      background-color: #f9f9f9;
    }

    header, section, footer {
      margin-bottom: 30px;
    }

    h1 {
      color: #2c3e50;
    }

    button {
      margin: 10px 5px;
      padding: 10px 15px;
      background-color: #0077cc;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #005fa3;
    }

    .dynamic-box {
      background-color: #eee;
      margin-top: 10px;
      padding: 10px;
      border-left: 4px solid #0077cc;
    }

    #main-title {
      transition: all 0.3s ease;
    }
  </style>
</head>
<body>

  <header>
    <h1 id="main-title">Welcome to My Interactive Page</h1>
  </header>

  <section>
    <p id="message">This is a simple paragraph that can be changed using JavaScript.</p>
    <button onclick="changeText()">Change Text</button>
    <button onclick="changeStyle()">Change Style</button>
  </section>

  <section>
    <button onclick="addElement()">Add Element</button>
    <button onclick="removeElement()">Remove Element</button>
    <div id="dynamic-container"></div>
  </section>

  <footer>
    <p>&copy; 2025 My Website. All rights reserved.</p>
  </footer>

  <script>
    // Change the text content of an element
    function changeText() {
      const msg = document.getElementById('message');
      msg.textContent = "The paragraph text has been updated!";
    }

    // Modify the style of an element
    function changeStyle() {
      const title = document.getElementById('main-title');
      title.style.color = "#d4af37";
      title.style.fontSize = "36px";
      title.style.textAlign = "center";
    }

    // Add a new element dynamically
    function addElement() {
      const container = document.getElementById('dynamic-container');
      const newDiv = document.createElement('div');
      newDiv.textContent = "New element added!";
      newDiv.className = "dynamic-box";
      container.appendChild(newDiv);
    }

    // Remove the last added element
    function removeElement() {
      const container = document.getElementById('dynamic-container');
      if (container.lastChild) {
        container.removeChild(container.lastChild);
      }
    }
  </script>

</body>
</html>


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
