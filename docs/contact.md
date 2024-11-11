# Contact API Spec

## Create Contact

Endpoint : POST /api/contacts

Request Header:
X-API-TOKEN : token

Request Body :

```json
{
  "first_name": "name contact",
  "last_name": "name contact",
  "email": "name@example.com",
  "phone": "012345678"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "name contact",
    "last_name": "name contact",
    "email": "name@example.com",
    "phone": "012345678"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Data invalid"
}
```

## Get Contact

Endpoint : GET /api/contacts/:id

Request Header:
X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "name contact",
    "last_name": "name contact",
    "email": "name@example.com",
    "phone": "012345678"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Data invalid"
}
```

## Update Contact

Endpoint : PUT /api/contacts/:id

Request Header:
X-API-TOKEN : token

Request Body :

```json
{
  "first_name": "name contact",
  "last_name": "name contact",
  "email": "name@example.com",
  "phone": "012345678"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "first_name": "name contact",
    "last_name": "name contact",
    "email": "name@example.com",
    "phone": "012345678"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Data invalid"
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/:id

Request Header:
X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "Success Remove Contact"
}
```

Response Body (Failed) :

```json
{
  "errors": "Data invalid"
}
```

## Search Contact

Endpoint : GET /api/contacts

Request Header:
X-API-TOKEN : token

Query Parameter :

- name : string, contact first name or contact last name, optional
- phone : string, phone number, optional
- email : string, contact email, optional
- page : number, default 1
- size : number, default 10

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "name contact",
      "last_name": "name contact",
      "email": "name@example.com",
      "phone": "012345678"
    },
    {
      "id": 2,
      "first_name": "name contact",
      "last_name": "name contact",
      "email": "name@example.com",
      "phone": "012345678"
    }
  ],
  "pagging": {
    "current_page": 1,
    "total_page": 10,
    "size": 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unathorized"
}
```
