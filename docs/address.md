# address API Spec

## Create Address

Endpoint : POST api/contacts/:idContats/addressess

Request Header :
X-API-TOKEN : TOKEN

Request Body :

```json
{
  "street": "Street Name",
  "city": "City Name",
  "province": "province Name",
  "country": "Country Name",
  "postal_code": "1234567"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street Name",
    "city": "City Name",
    "province": "province Name",
    "country": "Country Name",
    "postal_code": "1234567"
  }
}
```

Request Body :

```json
{
  "street": "Street Name",
  "city": "City Name",
  "province": "province Name",
  "country": "Country Name",
  "postal_code": "1234567"
}
```

Response Body (Failed)

```json
{
  "errors": "Data Invalid"
}
```

## Get Address

Endpoint : PUT api/contacts/:idContats/addressess/:idAddresses

Request Header :
X-API-TOKEN : TOKEN

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street Name",
    "city": "City Name",
    "province": "province Name",
    "country": "Country Name",
    "postal_code": "1234567"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "Data Invalid"
}
```

## Update Address

Endpoint : GET api/contacts/:idContats/addressess/:idAddresses

Request Header :
X-API-TOKEN : TOKEN

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Street Name",
    "city": "City Name",
    "province": "province Name",
    "country": "Country Name",
    "postal_code": "1234567"
  }
}
```

Response Body (Failed)

```json
{
  "errors": "Data Invalid"
}
```

## Remove Address

Endpoint : DELETE api/contacts/:idContats/addressess/:idAddresses

Request Header :
X-API-TOKEN : TOKEN

Response Body (Success) :

```json
{
  "data": "Data has deleted"
}
```

Response Body (Failed)

```json
{
  "errors": "Data Invalid"
}
```

## List Address

Endpoint : GET api/contacts/:idContats/addressess/

Request Header :
X-API-TOKEN : TOKEN

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "street": "Street Name",
      "city": "City Name",
      "province": "province Name",
      "country": "Country Name",
      "postal_code": "1234567"
    },
    {
      "id": 2,
      "street": "Street Name",
      "city": "City Name",
      "province": "province Name",
      "country": "Country Name",
      "postal_code": "1234567"
    }
  ]
}
```

Response Body (Failed)

```json
{
  "errors": "Data Invalid"
}
```
