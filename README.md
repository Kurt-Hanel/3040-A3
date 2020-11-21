# Folklorma API 

## Description 

This API provides access to essential information for the current year's Folklorama festival. For instance, requests to this API can yield general festival information, such as the start date, as well as individual pavilion information.

## Endpoints 

#### GET /pavilions/
Request the list of all pavilions which are open this year or the information for a specific one.  

##### Parameters
- none, or
- parameter `name` which is the name as given in the list of all pavilions

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

#### GET /availability/ 

Request the number of tickets are remaining for a specific pavilion.

##### Parameters
- parameter `name` which is the name of the pavilion of interest

##### Resources
``` json
{
    "id": "pavilion_id",
    "name": "pavilion_name",
    "year": 2021,
    "Location": "pavilion_Location",
    "tickect left": "10"
}
```

#### GET /info/
Request the generic information about this year's Folklorama.

##### Parameters
- none

##### Resources
```json
{
    "startDate": "2021-07-31",
    "endDate": "2021-08-12",
    "numberOfPavilions": 43,
    "phoneNumber": "204-982-6210",
    "email": "info@folklorama.ca"
}
```

#### GET /popular/
Fetch the current list of the top 10 most popular pavilions for this year's Folklorama.

##### Parameters
- none

##### Resources

```json
{
    "pavilions": [
        "name1",
        "name2",
        "name3",
        "name4",
        "name5",
        "name6",
        "name7",
        "name8",
        "name9",
        "name10"
    ]
}
```

## Examples

### Request

GET/availability?name=Africa

### Response

```json
{
    "id": "1",
    "name": "Africa",
    "fullName": "Africa Pavilion",
    "location": "194 Enfield Crescent",
    "availableTickets": 30,
    "url": "https://https://folklorama.tixit.ca/Online/default.asp?doWork::WScontent::loadArticle=Load&BOparam::WScontent::loadArticle::article_id=DC6C4B01-CDD6-41A5-B788-3FA4958624F5"
}
```
        
