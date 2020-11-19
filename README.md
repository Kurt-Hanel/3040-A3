# Folklorma API 

## Description 

This API provides access to essential information for the current year's Folklorama festival. For instance, requests to this API can yield general festival information, such as the start date, as well as individual pavilion information.

## Endpoints 

#### GET pavilions/
- No parameter: gets all pavilions 
- If parameter `name` is present: return details of specific pavilion (dates, times, location)

##### Parameters

##### Resources

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

GET availability [African Pavilion]

### Response

{
    "page": 1,
    "per_page": 6,
    [
        {
            "id": 1,
            "name": "Africa Pavilion",
            "year": 2019,
            "Location": "Located off St. Mary’s Rd, turn on to Enfield Cr",
            "ticket left": 30,
            
            
        }
        ],
        "support": {
        "url": "https://https://folklorama.tixit.ca/Online/default.asp?doWork::WScontent::loadArticle=Load&BOparam::WScontent::loadArticle::article_id=DC6C4B01-CDD6-41A5-B788-3FA4958624F5",
        "text": "Check the url for more info."
    }
}
        
