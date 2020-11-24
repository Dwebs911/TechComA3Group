# Manitoba API

## What is Manitoba API?
Manitoba API is a trend setting API that allows you to obtain information about anywhere or everywhere in Manitoba! We provide a simple one endpoint interface that can be filtered to specific locations using our various parameters. Our API allows its users to enter in a location with varying levels of accuracy and recieve helpful information about the surrounding area.

## API documentation

### Endpoints
To use our API we have 1 endpoint that is a GET request

> Generic Info  **https://api.manitoba.ca/Ginfo**

To call using a parameter:
>  **https://api.manitoba.ca/Ginfo/param1/**


To call using multiple parameters:
>  **https://api.manitoba.ca/Ginfo/param1/param2/param3**

GenericInfo can take any parameter and will return various generic facts about the location if found. If no location is specified it will return generic information about all cities in Manitoba. When using multiple parameters the information for the most specific one will be used.

#### Parameters
- City (String) The City parameter is used to specify the location of a city that you want to obtain the information of. **Optional**
- Address (String) Address allows you to focus in on a specific area of the city. If the address is found the information will be limited to a 10km radius of the address. **Optional**
- PostalCode (String) PostalCode allows you to focus in on a specific area of the city. If the postal code is found the information will be limited to a 10km radius of the postal code. **Optional**


#### Sample Calls
> https://api.manitoba.ca/Ginfo/Winnipeg


> https://api.manitoba.ca/Ginfo

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

If an address, city, or postal code are specified in a call but not found, an error code will be returned.

#### Sample Response
##### JSON

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

Call

> https://api.manitoba.ca/Ginfo/sgdjshdfs

Response

> { 
	"results:
	{
	}
	"status":"400 Bad Request"
}

