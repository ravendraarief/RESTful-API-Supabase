# user-specs

## Register User

Endpoint : POST /api/users

request Body :

```Json
{
  "username" : "Chooseyourusername",
  "password" : "chooseyourpassword",
  "name" : "Chooseyourname"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "Chooseyourusername",
    "name": "Chooseyourname"
  }
}
```

Response (Error) :

```json
{
  "errors": "data invalid"
}
```

## Login User

Endpoint : POST /api/users/login

request Body :

```Json
{
  "username" : "Chooseyourusername",
  "password" : "chooseyourpassword",
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "Chooseyourusername",
    "name": "Chooseyourname",
    "token": "generatetoken"
  }
}
```

Response (Error) :

```json
{
  "errors": "data invalid"
}
```

## Get User

Endpoint : GET /api/users/current

Request header : Token

Response Body (Success) :

```json
{
  "data": {
    "username": "Chooseyourusername",
    "name": "Chooseyourname"
  }
}
```

Response (Error) :

```json
{
  "errors": "unauthorized"
}
```

## Update User

Endpoint : PATCH /api/users/curent

Request header :
X-API-Token = generated token

request Body :

```Json
{
  "password" : "chooseyourpassword", //optional
  "name" : "Chooseyourname" //optional
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "Chooseyourusername",
    "name": "Chooseyourname"
  }
}
```

Response (Error) :

```json
{
  "errors": "data invalid"
}
```

## Logout User

Endpoint : POST /api/users/current

Request header :
X-API-Token = generated token

Response Body (Success) :

```json
{
  "data": "Logged out"
}
```

Response (Error) :

```json
{
  "errors": "data invalid"
}
```
