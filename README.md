# ISSTrackerHalf
# This is an unfinished code for tracking the international space station.
# Date: October 02, 2022

# Import Modules
import json
import urllib.request
import time
import geocoder
# Astronauts API
z = "PLACEHOLDER"
answer = urllib.request.urlopen(z)
result = json.loads(answer.read()) # Read API
Y = open("ISS_Tracker.txt") # Open Text File
# Number and Names
Y.write("There are currently" + str(result["number"]) + " astronauts on the ISS: \n\n") # Display the number of atronauts on board
names = result["PLACE HOLDER (before I find URL)"] # Names of Astronauts
# Declare longitude and latitude coordinates
geo = geocoder.ip('me')
Y.write("\n Your lat / long is: " + str(geo.latlng)) # Display latitude and longitude
