# Ex.08 Design of Interactive Image Gallery
# Date:06/05/2025
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
```
image.html

<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="UTF-8">

  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Interactive Image Gallery</title>

  <style>
  
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
      max-width: 900px;
      width: 100%;
    }

    .image-item img {
      width: 100%;
      height: auto;
      border-radius: 10px;
      transition: transform 0.3s ease;
    }

    .image-item img:hover {
      transform: scale(1.1);
      cursor: pointer;
    }
    .modal {
      display: none;
      position: fixed;
      z-index: 1;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(16, 16, 16, 0.8);
      justify-content: center;
      align-items: center;
    }

    .modal-content {
      max-width: 80%;
      max-height: 80%;
      margin: auto;
      display: block;
    }

    .close {
      position: absolute;
      top: 15px;
      right: 35px;
      color: #101010;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
    }

    .close:hover,
    .close:focus {
      color: #1e1c1c;
      text-decoration: none;
    }
  </style>

</head>

<body>

  <div class="gallery">

    <div class="image-item">

      <img src="image1.png" alt="Image 1">

    </div>

    <div class="image-item">

      <img src="image2.png" alt="Image 2">

    </div>

    <div class="image-item">

      <img src="image3.png" alt="Image 3">

    </div>

    <div class="image-item">

      <img src="image4.png" alt="Image 4">

    </div>

    <div class="image-item">

      <img src="image5.png" alt="Image 5">

    </div>

    <div class="image-item">

        <img src="image6.png" alt="Image 4">

      </div>

  </div>

  <div id="modal" class="modal">
    <span id="close" class="close">&times;</span>
    <img id="modal-img" class="modal-content" alt="Larger view">
  </div>

  <script>

    
    const modal = document.getElementById("modal");


    const modalImg = document.getElementById("modal-img");


    const images = document.querySelectorAll(".image-item img");


    const closeBtn = document.getElementById("close");


    images.forEach((image) => {

      image.addEventListener("click", () => {

        modal.style.display = "flex";

        modalImg.src = image.src;

      });

    });


    closeBtn.addEventListener("click", () => {

      modal.style.display = "none";

    });


    modal.addEventListener("click", (event) => {

      if (event.target === modal) {

        modal.style.display = "none";

      }

    });

  </script>

</body>

</html>
```

# OUTPUT:
![alt text](<Screenshot 2025-05-03 144819.png>)
![alt text](<Screenshot 2025-05-03 144831.png>)
![alt text](<Screenshot 2025-05-03 144843.png>)
![alt text](<Screenshot 2025-05-03 144904.png>)
![alt text](<Screenshot 2025-05-03 144936.png>)
![alt text](<Screenshot 2025-05-03 144945.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
