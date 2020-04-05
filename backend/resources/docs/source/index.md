---
title: API Reference

language_tabs:
- javascript
- php
- python
- bash

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.
[Get Postman Collection](http://localhost/docs/collection.json)

<!-- END_INFO -->

#Categories


<!-- START_80420c095ed96da032c9eb419d7d6e2d -->
## Get all categories

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/categories"
);

let params = {
    "page": "1",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'http://localhost/api/v1/categories',
    [
        'query' => [
            'page'=> '1',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/categories'
params = {
  'page': '1',
}
response = requests.request('GET', url, params=params)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/categories?page=1" 
```


> Example response (200):

```json
{
    "data": [
        {
            "id": 1,
            "name": "Quo velit id aut molestias."
        },
        {
            "id": 2,
            "name": "Velit aut repudiandae quis consequuntur aut."
        },
        {
            "id": 3,
            "name": "Dolor voluptas deleniti sit dolor sint consequatur."
        },
        {
            "id": 4,
            "name": "Nesciunt dolorem modi esse placeat."
        },
        {
            "id": 5,
            "name": "Rerum voluptatem voluptatem voluptatem expedita."
        }
    ],
    "links": {
        "first": "http:\/\/localhost\/api\/v1\/categories?page=1",
        "last": "http:\/\/localhost\/api\/v1\/categories?page=2",
        "prev": null,
        "next": "http:\/\/localhost\/api\/v1\/categories?page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 2,
        "path": "http:\/\/localhost\/api\/v1\/categories",
        "per_page": 5,
        "to": 5,
        "total": 10
    }
}
```

### HTTP Request
`GET api/v1/categories`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `page` |  optional  | The page number.

<!-- END_80420c095ed96da032c9eb419d7d6e2d -->

<!-- START_2378770b4f57b93f810abda7c44614b8 -->
## Get a single category
Retrieves a collection of entities that belong to the current category

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/categories/5"
);


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get('http://localhost/api/v1/categories/5');
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/categories/5'
response = requests.request('GET', url)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/categories/5" 
```


> Example response (200):

```json
{
    "data": {
        "name": "Rerum voluptatem voluptatem voluptatem expedita.",
        "entities": [
            {
                "id": 1,
                "name": "Aldea-Ignat",
                "country": "GL"
            },
            {
                "id": 3,
                "name": "Cucu-Toma",
                "country": "KZ"
            },
            {
                "id": 5,
                "name": "Iosif, Pascu and Baciu",
                "country": "SR"
            },
            {
                "id": 6,
                "name": "Barbulescu, Rosca and Baciu",
                "country": "BL"
            },
            {
                "id": 12,
                "name": "Ene Ltd",
                "country": "MZ"
            }
        ]
    }
}
```

### HTTP Request
`GET api/v1/categories/{category}`

#### URL Parameters

Parameter | Status | Description
--------- | ------- | ------- | -------
    `category` |  required  | The ID of the category.

<!-- END_2378770b4f57b93f810abda7c44614b8 -->

#Entities


<!-- START_4288e7337688d08ee1ca084a9b8a3b76 -->
## Get all entities

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/entities"
);

let params = {
    "page": "1",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'http://localhost/api/v1/entities',
    [
        'query' => [
            'page'=> '1',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/entities'
params = {
  'page': '1',
}
response = requests.request('GET', url, params=params)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/entities?page=1" 
```


> Example response (200):

```json
{
    "data": [
        {
            "id": 1,
            "name": "Aldea-Ignat",
            "country": "GL"
        },
        {
            "id": 2,
            "name": "Balint, Mirea and Stancu",
            "country": "MR"
        },
        {
            "id": 3,
            "name": "Cucu-Toma",
            "country": "KZ"
        },
        {
            "id": 4,
            "name": "Dragoi-Gavrila",
            "country": "MA"
        },
        {
            "id": 5,
            "name": "Iosif, Pascu and Baciu",
            "country": "SR"
        }
    ],
    "links": {
        "first": "http:\/\/localhost\/api\/v1\/entities?page=1",
        "last": "http:\/\/localhost\/api\/v1\/entities?page=100",
        "prev": null,
        "next": "http:\/\/localhost\/api\/v1\/entities?page=2"
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 100,
        "path": "http:\/\/localhost\/api\/v1\/entities",
        "per_page": 5,
        "to": 5,
        "total": 500
    }
}
```

### HTTP Request
`GET api/v1/entities`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `page` |  optional  | int The page number.

<!-- END_4288e7337688d08ee1ca084a9b8a3b76 -->

<!-- START_a1414f1a639a9d59798dede94d307873 -->
## Get a single entity

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/entities/2"
);


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get('http://localhost/api/v1/entities/2');
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/entities/2'
response = requests.request('GET', url)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/entities/2" 
```


> Example response (200):

```json
{
    "data": {
        "id": 2,
        "name": "Balint, Mirea and Stancu",
        "description": "Împăratul, cam de nevoie, răspunse: - Aşa o fi, se potriveşte ş-aşa, fiindcă ştii tu să cerni, şi ea să risipească, tu să pui de mămăligă, şi ea să răstoarne căldarea pe foc. - Dacă e pe-aşa, m-aş mulţumi şi pe-un copil cât ghemul, numai s-aud în casă \"mamă\", că mult e pustiu când uşa se închide peste doi bătrâni. - Da’ dacă ar fi mai mic?.",
        "type": "Beatae aperiam et et ut fugit eius id aliquid.",
        "categories": [
            "Quo velit id aut molestias.",
            "Velit aut repudiandae quis consequuntur aut.",
            "Dolor voluptas deleniti sit dolor sint consequatur.",
            "Nesciunt dolorem modi esse placeat.",
            "Reiciendis maxime occaecati est dolor ex."
        ],
        "location": {
            "address_line_1": "Calea Muncii 0A",
            "address_line_2": null,
            "city": "Sfântu Gheorghe",
            "county": "Arad",
            "postal_code": "917516",
            "country": "MR",
            "latitude": -53.359771,
            "longitude": -144.084054
        },
        "contact": {
            "email": "florea.staicu@example.net",
            "phone": "0355379914",
            "url": "http:\/\/ganea.info\/"
        }
    }
}
```

### HTTP Request
`GET api/v1/entities/{entity}`

#### URL Parameters

Parameter | Status | Description
--------- | ------- | ------- | -------
    `entity` |  required  | The ID of the entity.

<!-- END_a1414f1a639a9d59798dede94d307873 -->

#Entity Types


<!-- START_c8c46f79ea22771862059c1f7bcb0e64 -->
## Get all entity types

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/types"
);

let params = {
    "page": "1",
};
Object.keys(params)
    .forEach(key => url.searchParams.append(key, params[key]));


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get(
    'http://localhost/api/v1/types',
    [
        'query' => [
            'page'=> '1',
        ],
    ]
);
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/types'
params = {
  'page': '1',
}
response = requests.request('GET', url, params=params)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/types?page=1" 
```


> Example response (200):

```json
{
    "data": [
        {
            "id": 1,
            "name": "Beatae aperiam et et ut fugit eius id aliquid."
        },
        {
            "id": 2,
            "name": "Aut explicabo itaque id."
        },
        {
            "id": 3,
            "name": "Qui provident aperiam nesciunt non et reiciendis."
        }
    ],
    "links": {
        "first": "http:\/\/localhost\/api\/v1\/types?page=1",
        "last": "http:\/\/localhost\/api\/v1\/types?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "path": "http:\/\/localhost\/api\/v1\/types",
        "per_page": 5,
        "to": 3,
        "total": 3
    }
}
```

### HTTP Request
`GET api/v1/types`

#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    `page` |  optional  | The page number.

<!-- END_c8c46f79ea22771862059c1f7bcb0e64 -->

<!-- START_a90f973c81ffc9c1d05fa5beecb982b2 -->
## Get a single entity type
Retrieves a collection of entities that belong to the current type

> Example request:

```javascript
const url = new URL(
    "http://localhost/api/v1/types/3"
);


fetch(url, {
    method: "GET",
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get('http://localhost/api/v1/types/3');
$body = $response->getBody();
print_r(json_decode((string) $body));
```

```python
import requests
import json

url = 'http://localhost/api/v1/types/3'
response = requests.request('GET', url)
response.json()
```

```bash
curl -X GET \
    -G "http://localhost/api/v1/types/3" 
```


> Example response (200):

```json
{
    "data": {
        "name": "Qui provident aperiam nesciunt non et reiciendis.",
        "entities": [
            {
                "id": 3,
                "name": "Cucu-Toma"
            },
            {
                "id": 9,
                "name": "Banu, Sandor and Stefan"
            },
            {
                "id": 10,
                "name": "Grigore-Cristea"
            },
            {
                "id": 11,
                "name": "Ionescu, Catana and Chivu"
            },
            {
                "id": 19,
                "name": "Iliescu PLC"
            }
        ]
    }
}
```

### HTTP Request
`GET api/v1/types/{type}`

#### URL Parameters

Parameter | Status | Description
--------- | ------- | ------- | -------
    `type` |  required  | The ID of the entity type.

<!-- END_a90f973c81ffc9c1d05fa5beecb982b2 -->


