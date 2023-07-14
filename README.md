
# Import the required Module

import tabula

# Read a PDF File

df = tabula.read_pdf(r"C:\Users\hitha\Downloads\Andhra_Pradesh.pdf", pages='all')[0]

# convert PDF into CSV

tabula.convert_into(r"C:\Users\hitha\Downloads\Andhra_Pradesh.pdf", "A.csv", output_format="csv", pages='all')

print(df)

from geopy.geocoders import Nominatim

 

# calling the Nominatim tool

loc = Nominatim(user_agent="GetLoc")

 

# entering the location name

getLoc = loc.geocode("AndhraPradesh Srikakulam")

 

# printing address

print(getLoc.address)

 

# printing latitude and longitude

print("Latitude = ", getLoc.latitude, "\n")

print("Longitude = ", getLoc.longitude)


