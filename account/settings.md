# **Create Profile* #

Create Profile

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | PUT                                 |
| **Structure** | `/docter/api/:version/settings` |
| **Example**   | `/docter/api/v1/settings`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name        | Required | Type   | Default Value | Description                                 |
| ---------------   | -------- | ------ | ------------- | ------------------------------------------- |
| notification      | true     | String |               |                                             |
| sound             | true     | String |               |                                             |
| language          | true     | String |               |                                             |
| account_id        | true     | String |               |                                             |


## Example ##

```json
{
  "notification": true,
  "sound": false,
  "language": "th",
  "account_id":"docter:1234"
}
```
## Success Response ##

```json
{
  "data": {
    "status": "setting has been updated",
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
          "field": "notification",
          "reasons": ["is empty", "is required"]
        }
      ]
    }
  },
  "code": 400
}
```