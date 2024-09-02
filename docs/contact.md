# Contact API Spec

## Create Contact

Endpoint: POST /api/contacts

Headers:

- Authorization: token

Request Body:

```json
{
  "first_name": "Nama",
  "last_name": "Last name",
  "email": "email@gmail.com",
  "phone": "123456"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Nama",
    "last_name": "Last name",
    "email": "email@gmail.com",
    "phone": "123456"
  }
}
```

Response Body Error:

```json
{
  "errors": "Email is not valid"
}
```

## Update Contact

Endpoint: PUT /api/contacts/:id

Headers:

- Authorization: token

Request Body:

```json
{
  "first_name": "Nama",
  "last_name": "Last name",
  "email": "email@gmail.com",
  "phone": "123456"
}
```

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Nama",
    "last_name": "Last name",
    "email": "email@gmail.com",
    "phone": "123456"
  }
}
```

Response Body Error:

```json
{
  "errors": "Email is not valid"
}
```

## Get Contact

Endpoint: GET /api/contacts/:id

Headers:

- Authorization: token

Response Body Success:

```json
{
  "data": {
    "id": 1,
    "first_name": "Nama",
    "last_name": "Last name",
    "email": "email@gmail.com",
    "phone": "123456"
  }
}
```

Response Body Error:

```json
{
  "errors": "Contact not found"
}
```

## Search Contact

Endpoint: GET /api/contacts

Headers:

- Authorization: token

Query params:

- name: Search by first_name or last_name (optional)
- email: Search by email using like
- phone: Search by phone using like
- page: number of page, default: 1
- size: size per page, default: 10

Response Body Success:

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Nama",
      "last_name": "Last name",
      "email": "email@gmail.com",
      "phone": "123456"
    },
    {
      "id": 2,
      "first_name": "Nama",
      "last_name": "Last name",
      "email": "email@gmail.com",
      "phone": "123456"
    }
  ],
  "paging": {
    "page": 1,
    "total_page": 3,
    "total_item": 30
  }
}
```

Response Body Error:

## Delete Contact

Endpoint: DELETE /api/contacts/:id

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
