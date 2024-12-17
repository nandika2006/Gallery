# Ex.08 Design of Interactive Image Gallery
# Date: 17/12/2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :

index.html:

    <html lang="en">
      <head>
        <meta charset="UTF-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>interactive Image Gallery</title>
        <link rel="stylesheet" href="style.css" />
      </head>
      <body>
        <h1>Interactive Image Gallery</h1>
        <div class="image-container">
          <span style="--i: 1">
            <img
              src="download (8).jpeg"
            />
          </span>
          <span style="--i: 2">
            <img
              src="download (9).jpeg"
            />
          </span>
          <span style="--i: 3">
            <img
              src="download (10).jpeg"
            />
          </span>
          <span style="--i: 4">
            <img
              src="download (11).jpeg"
            />
          </span>
          <span style="--i: 5">
            <img
              src="download (12).jpeg"
            />
          </span>
          <span style="--i: 6">
            <img
              src="download (13).jpeg"
            />
          </span>
          <span style="--i: 7">
            <img
              src="download (14).jpeg"
            />
          </span>
          <span style="--i: 8">
            <img
              src="🥹🥹🐾🐾.jpeg"
            />
          </span>
        </div>
    
        <div class="btn-container">
          <button class="btn" id="prev">Prev</button>
          <button class="btn" id="next">Next</button>
        </div>
    
        <script src="app.js"></script>
      </body>
    </html>

style.css:
    
    body {
        margin: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        height: 100vh;
        background-color: bisque;
        overflow: hidden;
      }
      
      .image-container {
        position: relative;
        width: 200px;
        height: 200px;
        transform-style: preserve-3d;
        transform: perspective(1000px) rotateY(0deg);
        transition: transform 0.7s;
      }
      
      .image-container span {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px);
      }
      
      .image-container span img {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
      }
      
      .btn-container {
        position: relative;
        width: 80%;
      }
      
      .btn {
        position: absolute;
        bottom: -80px;
        background: crimson;
        color: #fff;
        border: none;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
      }
      
      #prev {
        left: 20%;
      }
      
      #next {
        right: 20%;
      }
      
      .btn:hover {
        filter: brightness(1.5);
      }

app.js:

    const imageContainer = document.querySelector(".image-container");
    const prevBtn = document.getElementById("prev");
    const nextBtn = document.getElementById("next");
    
    let x = 0;
    
    prevBtn.addEventListener("click", () => {
      x = x + 45;
      rotate();
    });
    
    nextBtn.addEventListener("click", () => {
      x = x - 45;
      rotate();
    });
    
    function rotate() {
      imageContainer.style.transform = `perspective(1000px) rotateY(${x}deg)`;
    }
# OUTPUT:

![image](https://github.com/user-attachments/assets/14d05569-5aab-493a-806c-b599e9aedd2e)
![image](https://github.com/user-attachments/assets/8829aa44-1981-4788-955a-f0475f5ead51)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
