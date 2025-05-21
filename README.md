# Ex.08 Design of Interactive Image Gallery
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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Image Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: gray;
      margin: 0;
      padding: 20px;
      text-align: center;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }

    .gallery img {
      width: 200px;
      height: 400px;
      object-fit: cover;
      cursor: pointer;
      border-radius: 5px;
      transition: transform 0.2s;
    }

    .gallery img:hover {
      transform: scale(1.05)
    }a

    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
    }

    .modal img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
    }

    .modal.active {
      display: flex;
    }

    .modal-close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h1>JavaScript Image Gallery</h1>

  <div class="gallery">
    <img src="img1.jpg" alt="Image 1">
    <img src="img2.jpg" alt="Image 2">
    <img src="img3.jpg" alt="Image 3">
    <img src="img4.jpg" alt="Image 4">
  </div>

  <div class="modal" id="imageModal">
    <span class="modal-close" id="closeModal">&times;</span>
    <img id="modalImg" src="" alt="Large View">
  </div>

  <script>
    const galleryImages = document.querySelectorAll('.gallery img');
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImg');
    const closeModal = document.getElementById('closeModal');

    galleryImages.forEach(img => {
      img.addEventListener('click', () => {
        modalImg.src = img.src.replace(/300|301|302|303/, '800');
        modal.classList.add('active');
      });
    });

    closeModal.addEventListener('click', () => {
      modal.classList.remove('active');
    });

    modal.addEventListener('click', (e) => {
      if (e.target === modal) {
        modal.classList.remove('active');
      }
    });
  </script>

</body>
</html>
```
# OUTPUT:
![Screenshot 2025-05-08 162022](https://github.com/user-attachments/assets/35c140dc-bf91-4fa3-94b8-80b71815e8db)

![Screenshot 2025-05-08 162044](https://github.com/user-attachments/assets/0e1b5e59-6eae-401e-8239-be9e83953ccf)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
