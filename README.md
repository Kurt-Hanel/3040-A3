# Folklorma API 

## Description 

This API provides access to essential information for the current year's Folklorama festival. For instance, requests to this API can yield general festival information, such as the start date, as well as individual pavilion information.

## Endpoints 

#### GET pavilions/
- No parameter: gets all pavilions 
- If parameter `name` is present: return details of specific pavilion 

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
