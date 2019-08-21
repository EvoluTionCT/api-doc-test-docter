# **Login Member** #

Forget Password

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/forget_password` |
| **Example**   | `/docter/api/v1/forget_password`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name | Required | Type   | Default Value | Description                                 |
| ---------- | -------- | ------ | ------------- | ------------------------------------------- |
| email      | true     | String |               |                                             |

## Example ##

```json
{
  "email": "test@scale360solutions.com"
}
```
## Success Response ##

```json
{
  "data": {
    "email": "test@test.com",
    "status": "success",
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