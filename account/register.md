# **Register** #

Register

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/register` |
| **Example**   | `/docter/api/v1/register`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name | Required | Type   | Default Value | Description                                 |
| ---------- | -------- | ------ | ------------- | ------------------------------------------- |
| email      | true     | String |               |                                             |
| password   | true     | String |               |                                             |

## Example ##

```json
{
  "email": "test@scale360solutions.com",
  "password": "Aa123456"
}
```

## Success Response ##

```json
{
  "data": {
    "id": "account:1234",
    "email": "test@test.com",
    "status": "new",
    "created_at": "2018-07-18T07:48:06.347Z",
    "updated_at": "2018-07-18T07:48:06.347Z"
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