# Project Responsive Web Design using Bootstrap
# Date:19.12.2025
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
pharm.html
{%load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>WellSpring Pharmacy</title>

 
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">

    
    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: #f9fafaa0;
            margin: 0;
        }

       
        .navbar {
            background-color: #ffffff;
            border-bottom: 1px solid #e0e0e0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
        }
        .navbar-brand {
            font-weight: bold;
            color: #198754 !important;
        }
        .nav-link {
            color: #333;
        }
        .nav-link:hover {
            color: #198754;
        }

        .hero {
            height: 190px;
            background: linear-gradient(135deg, #198754, #43c08a);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        .hero h2 {
            margin-bottom: 5px;
        }
        .hero p {
            margin-bottom: 10px;
        }

        
        .product-card {
            border: none;
            border-radius: 14px;
            overflow: hidden;
            background-color: #ffffff;
            transition: 0.3s;
            box-shadow: 0 6px 18px rgba(0,0,0,0.12);
        }
        .product-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 10px 28px rgba(0, 0, 0, 0.711);
        }
        .product-card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            display: block;
        }
        .card-body {
            text-align: center;
            padding: 12px 8px;
        }
        .card-body b {
            font-size: 14px;
        }
        .card-body p {
            font-size: 12px;
            color: #666;
        }

       
        footer {
            background-color: #198754;
            color: white;
            text-align: center;
            padding: 12px;
            margin-top: 30px;
        }
    </style>
</head>

<body>


<nav class="navbar navbar-expand-lg px-4">
    <a class="navbar-brand" href="#">WellSpring Pharmacy</a>

    <ul class="navbar-nav flex-row ms-4">
        <li class="nav-item me-3"><a class="nav-link" href="#">Medicines</a></li>
        <li class="nav-item me-3"><a class="nav-link" href="#">Health Care</a></li>
        <li class="nav-item me-3"><a class="nav-link" href="#">Prescription</a></li>
        <li class="nav-item me-3"><a class="nav-link" href="#">Contact</a></li>
    </ul>

    <form class="d-flex ms-auto">
        <input class="form-control me-2" type="search" placeholder="Search medicines">
        <button class="btn btn-success">Search</button>
    </form>
</nav>


<section class="hero text-white">
    <h2>Your Health, Our Priority</h2>
    <p>Trusted pharmacy for everyday wellness</p>
    <button class="btn btn-light px-4" onclick="showAlert()">Shop Now</button>
</section>


<div class="container my-5">
    <h4 class="mb-4 text-center">Popular Products</h4>

    <div class="row row-cols-1 row-cols-md-3 row-cols-lg-6 g-4">

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'pk.jpg'%}" alt="Pain Relief">
                <div class="card-body">
                    <b>Pain Relief</b>
                    <p>Tablets</p>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'cs.jpg'%}" alt="Cough Syrup">
                <div class="card-body">
                    <b>Cough Syrup</b>
                    <p>Cold Care</p>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'vit.jpg'%}" alt="Vitamins">
                <div class="card-body">
                    <b>Vitamins</b>
                    <p>Daily Health</p>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'fa.jpg'%}" alt="First Aid">
                <div class="card-body">
                    <b>First Aid</b>
                    <p>Emergency</p>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'bp.jpg'%}" alt="BP Monitor">
                <div class="card-body">
                    <b>BP Monitor</b>
                    <p>Home Care</p>
                </div>
            </div>
        </div>

        <div class="col">
            <div class="card product-card">
                <img src="{%static 'mask.jpg'%}" alt="Masks">
                <div class="card-body">
                    <b>Masks</b>
                    <p>Protection</p>
                </div>
            </div>
        </div>

    </div>
</div>


<footer>
    © 2025 WellSpring Pharmacy | Your Trusted Pharmacy
</footer>


<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>


<script>
    function showAlert() {
        alert("Welcome to WellSpring Pharmacy! Stay healthy 💚");
    }
</script>

</body>
</html>
```
```
urls.py
from django.urls import path
from pharmapp import views

urlpatterns = [
    path('', views.pharm, name='pharm'),
]
```
```
views.py
from django.shortcuts import render

def pharm(request):
    return render(request, 'pharm.html')
```
# OUTPUT:
![alt text](<Screenshot 2025-12-19 143733.png>)
# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
