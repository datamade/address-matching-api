address-matching-api
====================

### Query
/?search="123 Main St"

### JSON Response
```json
"results" : [
      {
         "address_components" : [ # the components of the matched address not the query address
            {
               "name" : "123",
               "types" : "address_number"
            },
            {
               "name" : "South Main St",
               "types" : [ "street_name" ]
            }]
         "formatted_address" : "123 South Main St", 
         "geometry" : {
            "location" : {
               "lat" : 87.42291810,
               "lng" : -42.08542120
            },
         "types" : [ "street_address" ] # let's start with just street addresses, not intersections or others
      }
   ],
   "status" : "OK" # if matches not found then, return NotFound status
}
```
