# Ex.07 Design of Interactive Image Gallery
## Date:24-03-2026

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
<html>
    <head>
        <title>Image Gallery</title>
        <style>
            body{
                background-color: rgb(200, 157, 239);
                justify-content: center;
                align-items: center;
            }
            .heading{
                text-align: center;
                font-size: xx-large;
                font-weight: bold;
                background-color: rgb(247, 227, 47);
            }
            .box{
                border: solid 5px black;
                width: 350px;
                height: 350px;
                background-color: rgb(243, 218, 52);
                margin-top: 200px;
                margin-left: 600px;
            }
            .buttons{
                display: flex;
                justify-content: space-around;
            }
            h3{
                display: flex;
                justify-content: center;
            }
            .image{
                margin-left: 25px;
                margin-top: 15px;
            }
            footer{
                position: fixed;
                bottom: 0;
                width: 100%;
                background-color: rgb(246, 239, 41);
                text-align: center;
                left: 0;
            }
        </style>
    </head>
    <body>
        <div class="heading">Image Gallery</div>
        <hr>
        <div class="box">
            <div class="image">
                <img src="Deer.avif" id="imgid" width="300" height="250">
            </div>
            <h3 id="captid"></h3>
            <div class="buttons">
                <button onclick="prev()">Prev</button>
                <button onclick="next()">Next</button>
            </div>
        </div>
        <footer>&copy; Moushmitha B(25014643)</footer>
        <script>
            let Index=0
            var Images=[
                {source: "Deer.avif",caption:"BABY DEER: Fawn"},
                {source: "Fox.avif",caption:"BABY FOX: Kit"},
                {source: "Koala.jpg",caption:"BABY KOALA: Joey"},
                {source: "panda.jpg",caption:"BABY PANDA: Cub"},
                {source: "puppy.avif",caption:"BABY DOG: Puppy"}
            ];
            function display()
            {
                document.getElementById("imgid").src=Images[Index].source;
                document.getElementById("captid").innerHTML=Images[Index].caption;
            }
            function prev()
            {
                Index--;
                if(Index<0)
                   Index=Images.length-1;
                display();
            }
            function next()
            {
                Index++;
                if(Index>=Images.length)
                    Index=0;
                display();
            }
        </script>
    </body>
</html>

```

## OUTPUT:
![alt text](<Screenshot (56).png>)
![alt text](<Screenshot (57).png>)
![alt text](<Screenshot (58).png>)
![alt text](<Screenshot (59).png>)
![alt text](<Screenshot (60).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
