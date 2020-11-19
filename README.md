# Manitoba API

## What is Manitoba API?
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam luctus ipsum non dui dignissim, ut maximus quam volutpat. Curabitur luctus vestibulum lacus quis pulvinar. Fusce laoreet lacus ante, eu consequat justo porta id. Cras fringilla in sem quis volutpat. Donec tristique dui vel imperdiet finibus. Aliquam ex justo, consequat a orci ac, mollis accumsan sapien. In vitae mauris id neque blandit pretium.

## API documentation

### Endpoints
To use our API you only have to do a GET request to  **https://api.manitoba.ca/json**.

#### Parameters
- Param1 (int) This is an int value. Required
- Param2 (string) This is an string value. Optional

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
      },  
       "status":"OK"  
    }


