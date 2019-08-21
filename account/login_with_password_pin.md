# **Login Member** #

Login Member

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/authentications` |
| **Example**   | `/docter/api/v1/authentications`       |


## Data Params (if `grant_type` field is 'password') ##

| Field Name | Required | Type   | Default Value | Description                                 |
| ---------- | -------- | ------ | ------------- | ------------------------------------------- |
| type       | true     | String |               |  type are support only (password, pin)      |
| email      | true     | String |               |                                             |
| password   | true     | String |               |                                             |

## Example ##

```json
{
  "type": "password",
  "email": "test@scale360solutions.com",
  "password": "Aa123456"
}
```
## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'pin') ##

| Field Name | Required | Type   | Default Value | Description                                 |
| ---------- | -------- | ------ | ------------- | ------------------------------------------- |
| type       | true     | String |               |  type are support only (password, pin)      |
| email      | true     | String |               |                                             |
| pin        | true     | String |               |                                             |

## Example ##

```json
{
  "type": "password",
  "email": "test@testing.com",
  "pin": "1234"
}
```

## Success Response ##

```json
{
  "data": {
    "email": "test@test.com",
    "status": "active",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoidXNlcjpmYzBmOTI5Yi1jZjRmLTRjNjItOGE3Ny1lODM2M2RhMzM1NDciLCJ1aWQiOjEsImV4cCI6MTUyMTEwMjQ4NH0.4-hsswP58kENvlYMEyiguAHLkNLnmdH8GWqIwoP48mU"
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
          "field": "pin",
          "reasons": ["is empty", "is required"]
        }
      ]
    }
  },
  "code": 400
}
```