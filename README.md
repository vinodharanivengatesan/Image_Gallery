# Ex.07 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Interactive Image Gallery</title>

    <style>
        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family:Arial, Helvetica, sans-serif;
        }

        body{
            background:white;
        }

        .header{
            width:100%;
            background:#1f3a8a;
            color:white;
            text-align:center;
            padding:18px;
            font-size:32px;
            font-weight:bold;
        }

        .container{
            height:85vh;
            display:flex;
            justify-content:center;
            align-items:center;
        }
        
        .gallery-card{
            background:#1c0202;
            padding:20px;
            border-radius:15px;
            width:420px;
            text-align:center;
            box-shadow:0 4px 10px rgba(0,0,0,0.2);
        }

  

        .gallery-card img{
            width:100%;
            height:400px;
            object-fit:cover;
            border-radius:10px;
        }

        .caption{
            margin-top:15px;
            font-size:28px;
            color:whitesmoke;
        }

        .buttons{
            margin-top:20px;
        }

        button{
            background:#4f46e5;
            color:white;
            border:none;
            padding:12px 22px;
            margin:0 10px;
            border-radius:10px;
            font-size:18px;
            cursor:pointer;
            transition:0.3s;
        }

        button:hover{
            background:#3730a3;
        }
    </style>
</head>

<body>

    <div class="header">
        Interactive Image Gallery
    </div>

    <div class="container">

        <div class="gallery-card">

            <img id="galleryImage" src="pic1.png" alt="Gallery Image">

            <div class="caption" id="caption">
                klaus michaelson
            </div>

            <div class="buttons">
                <button onclick="previousImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>

        </div>

    </div>

    <script>

        const gallery = [

            {
                image:"pic1.png",
                text:"KLAUS MICHAELSON"
            },

            {
                image:"pic2.png",
                text:"STEFAN SALVATORE"
            },

            {
                image:"pic3.png",
                text:"DAMON SALVATORE"
            },

            {
                image:"pic4.png",
                text:"ELENA"
            }

            


        ];

        let currentIndex = 0;

        const image = document.getElementById("galleryImage");
        const caption = document.getElementById("caption");

        function showImage(index){
            image.src = gallery[index].image;
            caption.innerText = gallery[index].text;
        }

        function nextImage(){

            currentIndex++;

            if(currentIndex >= gallery.length){
                currentIndex = 0;
            }

            showImage(currentIndex);
        }

        function previousImage(){

            currentIndex--;

            if(currentIndex < 0){
                currentIndex = gallery.length-1;
            }

            showImage(currentIndex);
        }

    </script>

</body>
</html>
```

## OUTPUT
<img width="1870" height="856" alt="Screenshot 2026-05-28 222748" src="https://github.com/user-attachments/assets/8eaf2e61-5b0a-4fe0-b21e-5c9146954607" />


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
