# **Upload Profile Picture* #

# **Create Profile* #

Create Profile

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/upload_profile_picture` |
| **Example**   | `/docter/api/v1/upload_profile_picture`       |

## Header Params

| Key              | Value            | Required | Description                                                          |
| ---------------- | ---------------- | -------- | -------------------------------------------------------------------- |
| Content-Type     | application/json | true     |                                                                      |


## Data Params (if `grant_type` field is 'password') ##

| Field Name      | Required | Type   | Default Value | Description                                 |
| --------------- | -------- | ------ | ------------- | ------------------------------------------- |
| url_picture      | true     | String |               |                                             |

## Example ##

```json
{
  "url_picture": "first",
}
```
## Success Response ##

```json
{
  "data": {
    "status": "upload picture profile success",
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

## URL ##

|               |                                      |
| ------------- | ------------------------------------ |
| **Method**    | POST                                 |
| **Structure** | `/docter/api/:version/create_profile` |
| **Example**   | `/docter/api/v1/create_profile`       |


## Data Params (if `grant_type` field is 'password') ##

| Field Name      | Required | Type   | Default Value | Description                                 |
| --------------- | -------- | ------ | ------------- | ------------------------------------------- |
| first_name      | true     | String |               |                                             |
| last_name       | true     | String |               |                                             |
| date_of_birth   | true     | String |               |                                             |
| address         | true     | String |               |                                             |
| id_card_number  | true     | String |               |                                             |
| id_card_picture  | true    | url file picture |               |                                             |

## Example ##

```json
{
  "first_name": "first",
  "last_name": "last",
  "date_of_birth": "2/1/1990",
  "address":"123",
  "id_card_number": "1234",
  "id_card_picture": "www.google.com",
}
```
## Success Response ##

```json
{
  "data": {
    "email": "test@test.com",
    "status": "created profile success",
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