# Ex.06 Book Front Cover Page Design
# Date:09/11/2024
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
```
<html>
<header>
    <title>
        Money Book</title>
</header>

<style>
    
    
      body {
            font-family: Arial, sans-serif;
            background-color: white;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

    .container {
            text-align: center;
            border: 1px solid #ddd;
            box-shadow: 5px 5px 15px rgba(7, 7, 7, 0.812);
            padding: 20px;
            width: 30%;
            position: relative;
            background-color:rgb(218, 224, 224);
        }
       /*
        .container::before,
        .container::after {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            width: 10px;
            background-color: green;
        }

        .container::before {
            left: -10px;
        }

        .container::after {
            right: -10px;
        } */

        .container {
            position: relative;
            background-color: #fff; 
            border: 2px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.2); 
            margin: 50px auto;
            z-index: 10;
            overflow: hidden; 
        }

        .container::before,
        .container::after {
            content: '';
            position: absolute;
            background-color: #f9f9f9;
            border: 1px solid #eee;
            transform: rotate(-2deg);
            z-index: -1;
            box-shadow: 0 8px 10px rgba(0, 0, 0, 0.15); 
        }
        .container::after {
            top: 10px;
            left: 10px;
            transform: rotate(-4deg);
        }

    .txt {
        text-align: center;
        font-size: 47px;
        font-weight: lighter;
        font-style: italic;
        
    }

    .txt1 {
        text-align: center;
        font-size: 60px;
        font-weight: bold;
        font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        word-spacing: 50px;
        
    }
    .txt2 {
        text-align: center;
        font-size: 80px;
        font-weight: bold;
        color:rgba(95, 149, 85, 0.666);
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        
    }

      .center {
        display: block;
        margin-left: 28%;
    }
    .author {
        font-size:20px;
        font-weight: bold;
            margin-bottom: 20px;
            word-spacing: 10px;
        }
    .nor {
        text-align: center;
        font-size: 30px;
        font-weight: lighter;
margin-left: 20%;
    }

    .txt3 {
        text-align: center;
        font-size: 60px;
    }
    img{
        border: none;
        border-color: white;
    }
</style>


<body>
    
            <div class="container">
               
               <div class="frst line" style=" word-spacing: 5px; letter-spacing: 5px; color:rgba(70, 180, 51, 0.666);"><p>OVER TWO  MILLION COPIES SOLD</p></div>
                <div class="txt">The</div>
                <div class="txt1"> Psychology </div><br>
                <div class="txt">of </div>
                <div class="title txt2">Money</div>
                <div class="graphic"></div>
                {% load static %}
                <img src="{% static 'logo.jpg' %}" width="40%" height="200px">
                <br> <br>
                <div class="subtitle" style="letter-spacing: 3px;">TIMELESS LESSONS ON WEALTH, GREED,<br> BRAND HAPPINESS</div><br>
                <div class="author"  style="letter-spacing: 5px;">MORGAN HOUSEL</div>
                <div style="margin-left: -5px;">&quot;Everyone should own a copy"</div>

                <a href="https://www.amazon.in/Psychology-Money-Morgan-Housel/dp/9390166268" style="margin-left: 50px;">Book</a> 
        
    </div>

</body>

</html>

views.py

from django.shortcuts import render
def image(request):
    return render(request,'book.html')

urls.py

from tempfile import template
from django.contrib import admin
from django.urls import path
from imagemap import views

urlpatterns = [
    path('map/',views.image),
]

# OUTPUT:
![Screenshot 2024-12-07 113051](https://github.com/user-attachments/assets/8fe1994e-e19a-4cf0-b9d7-1aff6445d90d)
![Screenshot 2024-12-07 114652](https://github.com/user-attachments/assets/dff46ffe-cf63-4f82-a977-b4bbd536ed54)


# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
