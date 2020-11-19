# Manitoba API

## What is Manitoba API?
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam luctus ipsum non dui dignissim, ut maximus quam volutpat. Curabitur luctus vestibulum lacus quis pulvinar. Fusce laoreet lacus ante, eu consequat justo porta id. Cras fringilla in sem quis volutpat. Donec tristique dui vel imperdiet finibus. Aliquam ex justo, consequat a orci ac, mollis accumsan sapien. In vitae mauris id neque blandit pretium.

## API documentation

### Endpoints
To use our API we have 1 endpoints both are GET requests

> Generic Info  **https://api.manitoba.ca/Ginfo**

GenericInfo can take any parameter and will return various generic facts about the location if found, If no location is found it will return generic information about all cities in manitoba.

#### Parameters
- City (String) The City parameter is used to specify the location that you want to obtain the information of. **Optional**
- Address (String) Address allows you to focus in on a specific area of the city. If the address is found the information will be limited to a 10km radius of the address. **Optional**
- PostalCode (String) PostalCode allows you to focus in on a specific area of the city. If the postal code is found the information will be limited to a 10km radius of the postal code. **Optional**

#### Sample Calls
> https://api.manitoba.ca/json?param1
> https://api.manitoba.ca/json?param1&param2

#### Response
##### JSON
> {
      "results":  
      {  
        "Param1":"204",  
        "Param2":"Manitoba"  
      } 
       "status":"OK"  
    }
    


