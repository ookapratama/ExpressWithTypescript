# User API Spesification

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "ookapratama",
  "password": "secret",
  "name": "Ooka Pratama",
  "Address": "Antang"
}
```

Response Body (Success):

```json
{
  "status": true,
  "data": {
    "username": "ookapratama",
    "name": "Ooka Pratama",
    "Address": "Antang"
  }
}
```

Response Body (Failed):

```json
{
  "status": false,
  "errors": "Username / Name / Address Cannot Empty!"
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "ookapratama",
  "password": "secret",
}
```

Response Body (Success):

```json
{
  "status": true,
  "data": {
    "username": "ookapratama",
    "name": "Ooka Pratama",
    "token": "uuid"
  }
}
```

Response Body (Failed):

```json
{
  "status": false,
  "errors": "Username / Name / Address Cannot Empty!"
}
```
## Get User

Endpoint : GET /api/users/get

Request Header : 
- X-API: token

Response Body (Success):

```json
{
  "status": true,
  "data": {
    "username": "ookapratama",
    "name": "Ooka Pratama",
    "address": "Antang"
  }
}
```

Response Body (Failed):

```json
{
  "status": false,
  "errors": "Unauthorized . . ."
}
```

## Update User

Endpoint : PATCH/PUT /api/users/get/

Request Header : 
- X-API: token

Request Body :

```json
{
  "username": "ookapratama", // tidak wajib
  "password": "secret", // tidak wajib
  "name" : "Ooka Pratama", // tidak wajib
  "address" : "Antang" // tidak wajib
}

Response Body (Success):

```json
{
  "status": true,
  "data": {
    "username": "ookapratama",
    "name": "Ooka Pratama",
    "address": "Antang"
  }
}
```

Response Body (Failed):

```json
{
  "status": false,
  "errors": "Unauthorized . . ."
}
```

## Logout User

Endpoint : DELETE /api/users/logouy

Request Header : 
- X-API: token

Response Body (Success):

```json
{
  "status": true,
  "data": "Berhasil Logout"
}
```

Response Body (Failed):

```json
{
  "status": false,
  "errors": "Unauthorized . . ."
}
```
