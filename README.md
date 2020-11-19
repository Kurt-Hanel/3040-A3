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

### Response

{
    "page": 1,
    "per_page": 6,
    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 1,
            "name": "Africa Pavilion",
            "year": 2019,
            "Location": "Located off St. Mary’s Rd, turn on to Enfield Cr",
            
        }
        
