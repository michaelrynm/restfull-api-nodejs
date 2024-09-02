# User API Spec

## Register User

Endpoint: POST /api/users

Request Body:

```json
{
  "username": "pzn",
  "password": "rahasia",
  "name": "nama"
}
```

Response Body Success:

```json
{
  "data": {
    "username": "pzn",
    "name": "nama"
  }
}
```

Response Body Error:

```json
{
  "errors": "Username already registered"
}
```

## Login User

Endpoint: POST /api/users/login

Request Body:

```json
{
  "username": "pzn",
  "password": "rahasia"
}
```

Response Body Success:

```json
{
  "data": {
    "token": "unique token"
  }
}
```

Response Body Error:

```json
{
  "errors": "Username or Password wrong"
}
```

## Update User

Endpoint: PATCH /api/users/current

Headers:

- Authorizatioin : Token

Request Body:

```json
{
  "name": "nama", //Optional
  "password": "new password" //Optional
}
```

Response Body Success:

```json
{
  "data": {
    "username": "pzn",
    "name": "nama"
  }
}
```

Response Body Error:

```json
{
  "errors": "Name length max 100"
}
```

## Get User

Endpoint: GET /api/users/current
Headers:

- Authorizatioin : Token

Response Body Success:

```json
{
  "data": {
    "username": "pzn",
    "name": "nama"
  }
}
```

Response Body Error:

```json
{
  "errors": "Unauthorized"
}
```

## Logout User
Endpoint: DELETE /api/users/logout
- Authorizatioin : Token

```json
{
  "data": "OK"
}
```
Response Body Error:

```json
{
  "errors": "Unauthorized"
}
```