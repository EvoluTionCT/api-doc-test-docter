# **Get Appointment* #

Create Profile

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/appointments` |
| **Example**   | `/docter/api/v1/appointments`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Authorization     | string            | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name            | Required | Type   | Default Value | Description                                 |
| ---------------       | -------- | ------ | ------------- | ------------------------------------------- |
| customer_name         | true     | String |               |                                             |
| office_name           | true     | String |               |                                             |
| start_time            | true     | String |               |                                             |
| end_time              | true     | String |               |                                             |   
| date                  | true     | String |               |                                             | 
| customer_image_left   | true     | String |               |                                             |   
| customer_image_front   | true     | String |               |                                             |
| customer_image_right   | true     | String |               |                                             | 
| customer_detail        | true     | Object |               |                                             |   
## Example ##

```json
{
    "customer_name":"Rata s",
    "office_name": "test clinic",
  "start_time": "19.00",
  "end_time": "20.00",
  "date": "2/1/1990",
  "customer_image_left": "url",
  "customer_image_left": "url",
  "customer_image_left": "url",
    "customer_detail": {}
}
```

## Error Response ##

```json
{
  "error": {
    "type":  "field_validation",
    "message": "field validation fail",
    "info": {
      "errors":  [
        {
          "field": "email",
          "reasons": ["is empty", "is required"]
        }
      ]
    }
  },
  "code": 400
}
```