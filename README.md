# Ex04 Places Around Me
# Date:30/9/2025
# AIM
To develop a website to display details about the places around my house.

# DESIGN STEPS
## STEP 1
Create a Django admin interface.

## STEP 2
Download your city map from Google.

## STEP 3
Using <map> tag name the map.

## STEP 4
Create clickable regions in the image using <area> tag.

## STEP 5
Write HTML programs for all the regions identified.

## STEP 6
Execute the programs and publish them.

# CODE
urls.py

from django.contrib import admin
from django.urls import path
from map import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.map),
    path('rail.html/',views.rail)
    ,path('rpc.html/',views.rpc)
    ,path('beach.html/',views.beach)
    ,path('metro.html/',views.metro)
    ,path('theatre.html/',views.theatre),
]

views.py


from django.shortcuts import render

# Create your views here.
def map(request):
    return render(request,"map.html")
def rail(request):
    return render (request,"rail.html")
def rpc(request):
    return render(request,"rpc.html")
def metro(request):
    return render(request,"metro.html")
def theatre(request):
    return render(request,"theatre.html")
def beach(request):
    return render(request,"beach.html")

map.html


{% load static %}
<title>Tvt map</title>
<body>
    <center><h1>Balaji T(25005672)</h1></center>
<img src="{% static 'map.png' %}" usemap="#image-map" border=5px>

<map name="image-map">
    <area shape="rect" coords="383,393,576,442" alt="Odeon Mani Theatre" href="theatre.html">
    <area shape="rect" coords="572,558,771,612" alt="Rpc school" href="rpc.html">
    <area shape="rect" coords="1207,404,1407,449" alt="Beach hangout spot" href="beach.html">
    <area shape="rect" coords="950,38,1102,98" alt="Theradi Metro" href="metro.html">
    <area shape="rect" coords="496,57,623,94" alt="Tvt railway" href="rail.html">
    <area shape="rect" coords="757,400,725,398" alt="Vijay " href="">
    <area shape="rect" coords="717,202,686,206" alt="Stalkspot" href="">
    <area shape="rect" coords="846,251,818,252" alt="house of coding god" href="">
    <area shape="rect" coords="947,363,917,362" alt="Our lady" href="">
    <area shape="rect" coords="775,580,749,579" alt="Sharmila" href="">
    <area shape="rect" coords="456,656,429,657" alt="F1 tharkuri lives here" href="">
</map>
</body>


beach.html

{%load static%}


<html>
    <head>
        <title>Theradi Metro</title>
    </head>

    <body style="background:linear-gradient(30deg,pink,blue)">
        <img src="{%static 'beach.png'%}" width="" height="50%" border=5px style="margin-left:auto;margin-right:auto;display:block"> 
        <center>
        <h1>Royapuram Rock Beach</h1> 
        <h2 align=left>
        <pre>
            Type:Tourist Spot
            address:toyapuram_beach, Tiruvottiyur, Chennai, Tamil Nadu 600019
            website: -
            about:
            Royapuram beach spot (often referred to as N4 Beach near Royapuram) is a quieter coastal stretch in northern Chennai
            , known for sea views near the Kasimedu fishing harbour. 
F
        </pre></h2></center>
 
    </body>
</html>


metro.html
{%load static%}


<html>
    <head>
        <title>Theradi Metro</title>
    </head>

    <body style="background:linear-gradient(30deg,pink,blue)">
        <img src="{%static 'metro.png'%}" width="" height="50%" border=5px style="margin-left:auto;margin-right:auto;display:block"> 
        <center>
        <h1>Theradi Metro station</h1> 
        <h2 align=left>
        <pre>
            Type: Public Transport
            address:Th Rd, Tiruvottiyur, Chennai, Tamil Nadu 600019
            website: https://cmrl.chennai.in
            about:
            Thiruvottiyur Theradi Metro station is an elevated station on Chennai Metro’s Blue Line,
             opened on 14 March 2022, serving the northern suburbs around Rajakadai / Kaladipet
        </pre></h2></center>
 
    </body>
rail.html
{%load static%}


<html>
    <head>
        <title>Theradi Metro</title>
    </head>

    <body style="background:linear-gradient(30deg,pink,blue)">
        <img src="{%static 'rail.png'%}" width="" height="50%" border=5px style="margin-left:auto;margin-right:auto;display:block"> 
        <center>
        <h1>Thiruvottriyur Railway Station</h1> 
        <h2 align=left>
        <pre>
            Type: Public Transport
            address:Thiruvottriyu Railway station, Tiruvottiyur, Chennai, Tamil Nadu 600019
            website: https://sr.indianrailways.gov.in/
            about:
            Thiruvottiyur railway station (TVT) is part of Chennai’s suburban network
             on the Chennai Central–Gummidipoondi line, with three platforms serving around 25,000 daily passengers
        </pre></h2></center>
 
    </body>
</html>
theatre.html
{%load static%}


<html>
    <head>
        <title>Theradi Metro</title>
    </head>

    <body style="background:linear-gradient(30deg,pink,blue)">
        <img src="{%static 'theatre.png'%}" width="" height="50%" border=5px style="margin-left:auto;margin-right:auto;display:block"> 
        <center>
        <h1>Odeon Mani Theatre</h1> 
        <h2 align=left>
        <pre>
            Type: Public Transport
            address:grama street, Tiruvottiyur, Chennai, Tamil Nadu 600019
            website: https://bookmyshow.in/odeonmani/
            about:
            Odeon Mani Theatre (also “Odiyan Mani Theatre”) is a single-screen cinema in
             Kaladipet, Tiruvottiyur, on W. Mada Street, showing movies with 2K/Dolby setups.
        </pre></h2></center>
 
    </body>
</html>

rpc.html

{%load static%}


<html>
    <head>
        <title>Rpc</title>
    </head>

    <body style="background:linear-gradient(30deg,pink,blue)">
        <img src="{%static 'rpc.png'%}" width="" height="50%" border=5px style="margin-left:auto;margin-right:auto;display:block"> 
        <center>
        <h1>Revoor Padmanabha Matriculation School</h1> 
        <h2 align=left>
        <pre>
            Type: Private School
            address:Rajakadai, Tiruvottiyur, Chennai, Tamil Nadu 600019
            website: https://revoorpadhmanabhachettysschool.in/
            about:
            Revoor Padmanabha Chetty Matriculation Higher Secondary School in Rajakadai, Thiruvottiyur, Chennai,
             is a co-educational English medium school established in 1983. 
            It offers classes up to +2 with good facilities and a strong academic reputation.
 .
        </pre></h2></center>
 
    </body>
</html>

    
# OUTPUT
# RESULT
The program for implementing image maps using HTML is executed successfully.
