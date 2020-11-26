# Folklorama API 

## Description 

This API provides access to essential information for the current year's Folklorama festival. For instance, requests to this API can yield general festival information, such as the start date, as well as individual pavilion information.

## Endpoints 

#### GET /pavilions/{name}
Request the list of all pavilions which are open this year or the information for a specific one.  

##### Parameters
- none, which will return all pavilions for this year
- an optional path parameter `name` which specifies a single pavilion
- an optional header parameter `popular` which is a boolean indicating if we should only return the 10 most popular pavilions

Note: if `name` is specified and `popular=true`, the popular flag is ignored in favour of returning the specified pavilion resource.

#### GET /info/
Request the generic information about this year's Folklorama.

##### Parameters
- none

### Festival
```json
{
    "startDate": "2021-07-31",
    "endDate": "2021-08-12",
    "numberOfPavilions": 43,
    "phoneNumber": "204-982-6210",
    "email": "info@folklorama.ca"
}
```

### Pavilion
```json
{
    "name": "Scandinavia",
    "location": "22 Jump Street",
    "times": [
        "6:00",
        "7:30",
        "9:00"
    ],
    "ticketsRemaining": 99,
    "startDate": "2021-07-31",
    "endDate": "2021-08-6"
}
``` 

### Pavilions 


```json
{
    "pavilions": [
        {
            "name": "Scotland",
            "location": "22 Jump Street",
            "times": [
                "6:00",
                "7:30",
                "9:00"
            ],
            "ticketsRemaining": 100,
            "startDate": "2021-07-31",
            "endDate": "2021-08-12"
        }
    ]
}
```


## Examples

### Request

GET /pavilions/Africa

### Response

```json
{
    "name": "Africe",
    "location": "21 Wall Street",
    "times": [
        "3:00",
        "8:30",
        "10:00"
    ],
    "ticketsRemaining": 50,
    "startDate": "2021-07-31",
    "endDate": "2021-08-6"
}
```
## Group 8

### Nabeel Saeed
### Kurt Hanel
### Matt Cameron
### Ronghan Wang
        
