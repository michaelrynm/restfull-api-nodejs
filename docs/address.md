## Address API Spec

# Create Address

Endpoint: POST /api/contacts/:contactId/adresses

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "jalan",
  "city": "Kota",
  "province": "Provinsi",
  "country": "Negara",
  "postal_code": "kode post"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "jalan",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postal_code": "kode post"
  }
}
```

Response Body Error:

```json
{
  "errors": "Country is required"
}
```

# Update Address

Endpoint: PUT /api/contacts/:contactId/adresses/:addressId

Headers:

- Authorization: token

Request Body:

```json
{
  "street": "jalan",
  "city": "Kota",
  "province": "Provinsi",
  "country": "Negara",
  "postal_code": "kode post"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "jalan",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postal_code": "kode post"
  }
}
```

Response Body Error:

```json
{
  "errors": "Country is required"
}
```

# Get Address

Endpoint: GET /api/contacts/:contactId/adresses/:addressId

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "street": "jalan",
    "city": "Kota",
    "province": "Provinsi",
    "country": "Negara",
    "postal_code": "kode post"
  }
}
```

Response Body Error:

```json
{
  "errors": "Contact not found"
}
```

# List Address

Endpoint: GET /api/contacts/:contactId/adresses

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "street": "jalan",
      "city": "Kota",
      "province": "Provinsi",
      "country": "Negara",
      "postal_code": "kode post"
    },
    {
      "id": 2,
      "street": "jalan",
      "city": "Kota",
      "province": "Provinsi",
      "country": "Negara",
      "postal_code": "kode post"
    }
  ]
}
```

Response Body Error:

```json
{
  "errors": "Contact not found"
}
```

# Remove Address

Endpoint: DELETE /api/contacts/:contactId/adresses/:addressId

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": "OK"
}
```

Response Body Error:

```json
{
  "errors": "Contact not found"
}
```
