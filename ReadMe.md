##API REST WITH KOTLIN AND SPRING BOOT
### GET

Url: `http://localhost:8080/customers`

#### Response (Status Code: 200 Ok)
```json
{
    "_embedded": {

        "customers": [
            {
                "firstName": "Felipe",
                "lastName": "Baz",
                "email": "baz@xds.com.br",
                "documentNumber": "123",
                "documentType": "CPF",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/customers/1"
                    },
                    "customer": {
                        "href": "http://localhost:8080/customers/1"
                    }
                }
            },
            {
                "firstName": "João",
                "lastName": "Baz",
                "email": "João@xds.com.br",
                "documentNumber": "1234",
                "documentType": "RG",
                "_links": {
                    "self": {
                        "href": "http://localhost:8080/customers/2"
                    },
                    "customer": {
                        "href": "http://localhost:8080/customers/2"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "http://localhost:8080/customers"
        },
        "profile": {
            "href": "http://localhost:8080/profile/customers"
        }
    },
    "page": {
        "size": 20,
        "totalElements": 2,
        "totalPages": 1,
        "number": 0
    }
}
```

### POST

Url: `http://localhost:8080/customers`

#### Body
```json
{
    "firstName": "Henrique",
    "lastName": "Baz",
    "documentNumber": "1234",
    "documentType": "RG",
    "email": "Henrique@xds.com.br"
}
```

#### Response (Status Code: 201 Created)
```json
{
    "firstName": "Henrique",
    "lastName": "Baz",
    "email": "Henrique@xds.com.br",
    "documentNumber": "1234",
    "documentType": "RG",
    "_links": {
        "self": {
            "href": "http://localhost:8080/customers/3"
        },
        "customer": {
            "href": "http://localhost:8080/customers/3"
        }
    }
}
```

### PUT

Url: `http://localhost:8080/customers/{Id}`

#### Body

```json
{
    "firstName": "João",
    "lastName": "Baz",
    "documentNumber": "1234",
    "documentType": "RG",
    "email": "João@xds.com.br"
}
```

#### Response (Status Code: 200 Ok)

```json
{
    "firstName": "João",
    "lastName": "Baz",
    "email": "João@xds.com.br",
    "documentNumber": "1234",
    "documentType": "RG",
    "_links": {
        "self": {
            "href": "http://localhost:8080/customers/2"
        },
        "customer": {
            "href": "http://localhost:8080/customers/2"
        }
    }
}
```

### Delete

Url: `http://localhost:8080/customers/{Id}`

#### Response (Status Code: 204 No Content)
