# Manitoba API

## What is Manitoba API?
Manitoba API is a trend setting API that provides information about anywhere or everywhere in Manitoba! It provides a simple one endpoint interface provides useful information about any specific location and surrounding area in Manitoba.

## API documentation

### Endpoints
Manitoba API has 1 endpoint that is a GET request

> Generic Info  **https://api.manitoba.ca/Ginfo**

To call using a parameter:
>  **https://api.manitoba.ca/Ginfo/param1/**


To call using multiple parameters:
>  **https://api.manitoba.ca/Ginfo/param1/param2/param3**

Ginfo uses parameters to determine location and will return various facts about the location if found. If no location is specified/found, Ginfo will return information about all cities in Manitoba. When using multiple parameters the most specific one will be used.

#### Parameters
- City (String) - Used to specify the location of a city that you want to obtain the information of. **Optional**
- Address (String) - Used to focus in on a specific area of the city. If the address is found the information will be limited to a 10km radius of the address. **Optional**
- PostalCode (String) - Used to focus in on a specific area of the city. If the postal code is found the information will be limited to a 10km radius of the postal code. **Optional**

#### Resources

Resources will be formatted in JSON and will be formatted as follows:

> {
      "results":  
      {  
        "TimeZoneWinnipeg":"GMT-6",
        "TemperatureWinnipeg":"-6 C"
        "NearbyStoresWinnipeg":"128"
        "WinnipegPopulation":"749,534"
      } 
       "status":"OK"  
    }

#### Sample Calls and Response

Call 

> https://api.manitoba.ca/Ginfo/Winnipeg

Response

> {
      "results":  
      {  
        "TimeZoneWinnipeg":"GMT-6",
        "TemperatureWinnipeg":" -6 C"
        "NearbyStoresWinnipeg":"128"
        "WinnipegPopulation":"749,534"
      } 
       "status":"OK"  
    }
   

Call 

> https://api.manitoba.ca/Ginfo/   

Response

> {
      "results":  
      {  
        "TimeZoneWinnipeg":"GMT-6",
        "TemperatureWinnipeg":"-6 C"
        "NearbyStoresWinnipeg":"128"
        "WinnipegPopulation":"749,534"   
        "TimeZoneBrandon":"GMT-6",
        "TemperatureBrandon":" -6 C"
        "NearbyStoresBrandon":"65"
        "BrandonPopulation":"48,859"
        "TimeZoneSelkirk":"GMT-6",
        "TemperatureSelkirk":" -6 C"
        "NearbyStoresSelkirk":"23"
        "SelkirkPopulation":"10,278"
      } 
       "status":"OK"  
    }

