# **Create Profile* #

Create Profile

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/add_schedule` |
| **Example**   | `/docter/api/v1/add_schedule`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name      | Required | Type   | Default Value | Description                                 |
| --------------- | -------- | ------ | ------------- | ------------------------------------------- |
| start_time      | true     | String |               |                                             |
| end_time        | true     | String |               |                                             |
| date            | true     | String |               |                                             |
| office          | true     | String |               |                                             |   
## Example ##

```json
{
  "start_time": "19.00",
  "end_time": "20.00",
  "date": "2/1/1990",
  "office": "boy clinic"
}
```
## Success Response ##

```json
{
  "data": {
    "status": "schedule has been created",
  },
  "code": 200
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