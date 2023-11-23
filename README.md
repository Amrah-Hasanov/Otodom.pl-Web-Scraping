# Otodom.pl Web Scraping

A web scraping project where I have used Beautiful Soup to extract product information of real estate properties from Otodom.pl (an online Polish real estate advertising website). Then, I have created a Tableau visualization with the scraped data. 

![fb-image200x200](https://github.com/Amrah-Hasanov/Otodom.pl-Web-Scraping/assets/145210183/405556a8-f06c-4693-a8b3-e739dfd444fb)

The code consits of mainly two parts: 
1. Defining fuctions for extracting the properties of listings that needs to be scraped. 
2. The request part, where I defined the headers, URL and add a scraping loop.

The data has 11 columns:


Title	- The title of the listing.

Price	- The price of the listing in (PLN).

Location	- The address values of the listing. 
In the website, the address information was added as a string with commas diving the voivodeship, city, county and street names of the address. (Like: ("ul. Ludwiki, Czyste, Wola, Warszawa, mazowieckie"). In other words, it wasn't possible to directly extract those values separately. So I just have created two new columns called Voivodeship and City in the data preprocessing part of the project in order to be able to assign geographic roles to the addresses of listed flats.

Surface	- The surface of the listed flats in (m²).

Number_of_Rooms	- The number of the rooms in the listed flats.

Floor	- The floor which the listed flats are located.

Finishing_Condition	- The living condition of the listed flat. Values: ("do zamieszkania", "do wykończenia", "do remontu", NaN). 
(In English translation: "for living", "to finish", NaN, "for renovation").

Heating	- The heating system that the listed flats have. Values: (miejskie, gazowe, inne, kotłownia, elektryczne, piece kaflowe, NaN).
(In English translation: urban, gas, other, boiler room, electric, tiled stoves, NaN).

Parking_Space	- The parking space of the listed flats. 
Values: ("garaż/miejsce parkingowe", NaN)                   

Balcony_Garden_Terrace - The Balcony, Garden and Terrace.
Values: (balkon, ogródek, taras) 

Link - The link of the ad

Voivodeship - Created Voivodeship values.

City - Created City values.

![Picture1](https://github.com/Amrah-Hasanov/Otodom.pl-Web-Scraping/assets/145210183/35a71b1f-df08-4853-ace7-2ca749760fe2)

You can find the visualisation of the collected data from my Tableau public account:
https://public.tableau.com/app/profile/amrah.hasanov/viz/FlatPricesinPoland/Dashboard1?publish=yes

In this link, the project dashboard can be found, and property prices can be compared across the voivodeships of Poland. And, variables such as the number of rooms, surface area, living conditions, etc., can be filtered to obtain more specific insights for your search.
