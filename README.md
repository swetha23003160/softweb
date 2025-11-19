# Ex.07 Restuarant Website
## Date:19.11.2025

## AIM:
To develop a static Resturant website to display the menu and services provided by the resturant.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
## home.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>The Midnight Spice | Home</title>
  <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
  <header>
    <h1>The Midnight Spice</h1>
    <nav>
      <a href="{% url 'home' %}" class="active">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'chefs' %}">Chefs</a>
      <a href="{% url 'contact' %}">Contact</a>
    </nav>
  </header>

  <section class="hero" style="background-image: url('{% static 'images/hero-bg.jpg' %}');">
    <div class="hero-inner">
      <h2>Serving Cravings After the Clock Strikes Midnight</h2>
      <p class="lead">Taste the Heat Hidden in the Night.</p>
      <button onclick="location.href='{% url 'menu' %}'">Explore Menu</button>
    </div>
  </section>

  <section class="teaser">
    <h3>Signature Picks</h3>
    <div class="grid">
      <div class="card">
        <img src="{% static 'images/gobi-manchurian.jpg' %}" alt="Gobi Manchurian">
        <p>Gobi Manchurian</p>
      </div>
      <div class="card">
        <img src="{% static 'images/pav-bhaji.jpg' %}" alt="Pav Bhaji">
        <p>Pav Bhaji</p>
      </div>
      <div class="card">
        <img src="{% static 'images/samosa-plate.jpg' %}" alt="Samosa">
        <p>Samosa Chaat</p>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 The Midnight Spice | Hot Bites. Cold Nights. Endless Cravings</p>
  </footer>
</body>
</html>

```
## menu.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>The Midnight Spice | Menu</title>
  <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
  <header>
    <h1>The Midnight Spice</h1>
    <nav>
      <a href="{% url 'home' %}">Home</a>
      <a href="{% url 'menu' %}" class="active">Menu</a>
      <a href="{% url 'chefs' %}">Chefs</a>
      <a href="{% url 'contact' %}">Contact</a>
    </nav>
  </header>

  <main class="menu">
    <h2>Our Menu — Veg Fast Food, Midnight Mood</h2>

    <section class="menu-section">
      <h3>Starters</h3>
      <div class="grid">
        <div class="item card">
          <img src="{% static 'images/gobi-manchurian.jpg' %}" alt="Gobi Manchurian">
          <h4>Gobi Manchurian</h4>
          <p>Crispy cauliflower tossed in tangy Indo-Chinese glaze</p>
          <span class="price">₹180</span>
        </div>

        <div class="item card">
          <img src="{% static 'images/samosa-plate.jpg' %}" alt="Samosa Chaat">
          <h4>Samosa Chaat</h4>
          <p>Spiced potatoes, chutneys, and crunch</p>
          <span class="price">₹80</span>
        </div>

        <div class="item card">
          <img src="{% static 'images/paneer-tikka.jpg' %}" alt="Paneer Tikka">
          <h4>Paneer Tikka</h4>
          <p>Smoky cubes, charred edges, mint chutney</p>
          <span class="price">₹170</span>
        </div>
      </div>
    </section>

    <section class="menu-section">
      <h3> Mains & Buns </h3>
      <div class="grid">
        <div class="item card">
          <img src="{% static 'images/pav-bhaji.jpg' %}" alt="Pav Bhaji">
          <h4>Pav Bhaji</h4>
          <p>Buttery pav with rich masala bhaji</p>
          <span class="price">₹140</span>
        </div>

        <div class="item card">
          <img src="{% static 'images/chole-bhature.jpg' %}" alt="Chole Bhature">
          <h4>Chole Bhature</h4>
          <p>Fluffy bhature with spicy chole</p>
          <span class="price">₹130</span>
        </div>

        <div class="item card">
          <img src="{% static 'images/dessert.jpg' %}" alt="Choco Lave Cake">
          <h4>Choco Lava Cake</h4>
          <p>Rich, creamy, finished with chocolate ash</p>
          <span class="price">₹300</span>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 The Midnight Spice | Taste the midnight flavor</p>
  </footer>
</body>
</html>

```
## chefs.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>The Midnight Spice | Chefs</title>
  <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
  <header>
    <h1>The Midnight Spice</h1>
    <nav>
      <a href="{% url 'home' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'chefs' %}" class="active">Chefs</a>
      <a href="{% url 'contact' %}">Contact</a>
    </nav>
  </header>

  <main class="chefs">
    <h2>Our Chefs</h2>
    <div class="grid">
      <div class="card">
        <img src="{% static 'images/chef1.jpg' %}" alt="Chef Meera">
        <h3>Chef Meera</h3>
        <p>Architect of the Gobi: smoke, crunch, and spice.</p>
      </div>
      <div class="card">
        <img src="{% static 'images/chef2.jpg' %}" alt="Chef Arjun">
        <h3>Chef Arjun</h3>
        <p>Master of street flavors with a midnight plating twist.</p>
      </div>
    </div>
  </main>

  <footer>
    <p>© 2025 The Midnight Spice | Craft & spice</p>
  </footer>
</body>
</html>

```
## contact.html
```
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>The Midnight Spice | Contact</title>
  <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>
  <header>
    <h1>The Midnight Spice</h1>
    <nav>
      <a href="{% url 'home' %}">Home</a>
      <a href="{% url 'menu' %}">Menu</a>
      <a href="{% url 'chefs' %}">Chefs</a>
      <a href="{% url 'contact' %}" class="active">Contact</a>
    </nav>
  </header>

  <main class="contact">
    <h2>Contact & Reservation</h2>
    <div class="contact-grid">
      <form class="contact-form">
        <input type="text" placeholder="Your Name" required>
        <input type="email" placeholder="Email" required>
        <input type="text" placeholder="Phone / WhatsApp" required>
        <textarea placeholder="Message / Reservation details"></textarea>
        <button type="submit">Send</button>
      </form>

      <div class="contact-info">
        <img src="{% static 'images/contact-bg.jpg' %}" alt="Restaurant Interior">
        <p>Visit us: Midnight Lane, City Center</p>
        <p>Open: 7PM — 2AM</p>
        <p>Phone: +91 90000 00000</p>
      </div>
    </div>
  </main>

  <footer>
    <p>© 2025 The Midnight Spice | Designed and Developed by pavithra</p>
  </footer>
</body>
</html>

```
## views.py
```
from django.shortcuts import render

def home(request):
    return render(request, 'home.html')

def menu(request):
    return render(request, 'menu.html')

def chefs(request):
    return render(request, 'chefs.html')

def contact(request):
    return render(request, 'contact.html')

```
## urls.py
```
from django.contrib import admin
from django.urls import path
from softapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.home, name='home'),
    path('menu/', views.menu, name='menu'),
    path('chefs/', views.chefs, name='chefs'),
    path('contact/', views.contact, name='contact'),
]
```
## OUTPUT:
<img width="1136" height="652" alt="image" src="https://github.com/user-attachments/assets/39f9d478-c955-45ca-9163-8f868ded6d21" />

<img width="1145" height="680" alt="image" src="https://github.com/user-attachments/assets/118be27f-0a70-47c3-8d9e-f983aae2228e" />

<img width="1141" height="687" alt="image" src="https://github.com/user-attachments/assets/a0d5c2a1-ebca-46a9-a70c-8f55ee74717c" />

<img width="1143" height="672" alt="image" src="https://github.com/user-attachments/assets/c15dd893-5881-4df0-8e98-bd183490a169" />

<img width="1138" height="637" alt="image" src="https://github.com/user-attachments/assets/413546ae-b91e-486d-9946-15c4cdf44c35" />

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
