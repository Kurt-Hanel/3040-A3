# Folklorma API 

## Description 

This API provides access to essential information for the current year's Folklorama festival. For instance, requests to this API can yield general festival information, such as the start date, as well as individual pavilion information.

## Endpoints 

#### GET pavilions/
Request the list of all pavilions which are open this year or the information for a specific one.  

##### Parameters
- no parameter, or
- parameter `name` where it is the name as given in the list of all pavilions

##### Resources
No parameter: 
```json
{
    "pavilions": [
        "name1",
        "name2"
    ]
}
```
`name` parameter:
```json
{
    "startDate": "2021-07-31",
    "endDate": "2021-08-12",
    "times": [
        "6:00",
        "7:30",
        "9:00"
    ],
    "location": "21 Jump Street"
}
``` 

#### GET availability/ 
- takes pavilion name as parameter
- returns the number of tickets left to purchase

#### GET info/
- returns general info for folklorama
- start date, end date, number of pavilions

#### GET popular
- lists the 10 most popular pavilions for the current festival based on number of tickets sold

## Examples

### Request

GET/availability/African

### Response

```{
   { "page": 1,
    "per_page": 6,
    [
        {
            "id": 1,
            "name": "Africa Pavilion",
            "year": 2019,
            "Location": "Located off St. Mary’s Rd, turn on to Enfield Cr",
            "ticket left": 30
            }
        ],
        "support": {
        "url": "https://https://folklorama.tixit.ca/Online/default.asp?doWork::WScontent::loadArticle=Load&BOparam::WScontent::loadArticle::article_id=DC6C4B01-CDD6-41A5-B788-3FA4958624F5",
        "text": "Check the url for more info."
    }}
    }
}```
        
