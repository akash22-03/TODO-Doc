---
title: Swagger ToDo v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="swagger-todo">Swagger ToDo v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

This is a sample ToDo server.  

Base URLs:


<a href="http://swagger.io/terms/">Terms of service</a>
Email: <a href="mailto:apiteam@swagger.io">Support</a> 
License: <a href="http://www.apache.org/licenses/LICENSE-2.0.html">Apache 2.0</a>

<h1 id="swagger-todo-items">Items</h1>

All your todos

<a href="http://swagger.io">Find out more</a>

## updateItem

<a id="opIdupdateItem"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem \
  -H 'Content-Type: application/json'

```

```http
PUT https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem HTTP/1.1
Host: virtserver.swaggerhub.com
Content-Type: application/json

```

```javascript
const inputBody = 'false';
const headers = {
  'Content-Type':'application/json'
};

fetch('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put 'https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/ToDo/upadteItem", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /ToDo/upadteItem`

*Update an existing item*

> Body parameter

```json
false
```

<h3 id="updateitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid ID supplied|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Validation exception|None|

<aside class="success">
This operation does not require authentication
</aside>

## findPetsByStatus

<a id="opIdfindPetsByStatus"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus?status=Completed \
  -H 'Accept: application/json'

```

```http
GET https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus?status=Completed HTTP/1.1
Host: virtserver.swaggerhub.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus?status=Completed',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus',
  params: {
  'status' => 'array[string]'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus', params={
  'status': [
  "Completed"
]
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus?status=Completed");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/findByStatus", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /Items/findByStatus`

*Finds items by status*

Multiple status values can be provided with comma separated strings

<h3 id="findpetsbystatus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|status|query|array[string]|true|Status values that need to be considered for filter|

#### Enumerated Values

|Parameter|Value|
|---|---|
|status|Completed|
|status|Pending|
|status|Deleted|

> Example responses

> 200 Response

```json
[]
```

```xml
<?xml version="1.0" encoding="UTF-8" ?>
```

<h3 id="findpetsbystatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|successful operation|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid status value|None|

<h3 id="findpetsbystatus-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|any|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## AddItemWithForm

<a id="opIdAddItemWithForm"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId} \
  -H 'Content-Type: application/x-www-form-urlencoded'

```

```http
POST https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId} HTTP/1.1
Host: virtserver.swaggerhub.com
Content-Type: application/x-www-form-urlencoded

```

```javascript
const inputBody = '{
  "desc": "string",
  "due": "string"
}';
const headers = {
  'Content-Type':'application/x-www-form-urlencoded'
};

fetch('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post 'https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/x-www-form-urlencoded'
}

r = requests.post('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/x-www-form-urlencoded',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/x-www-form-urlencoded"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/postItem/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /Items/postItem/{itemId}`

*Adds an item*

> Body parameter

```yaml
desc: string
due: string

```

<h3 id="additemwithform-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|itemId|path|string|true|item that needs to be updated|
|body|body|object|false|none|
|» desc|body|string|false|Updated description of the item|
|» due|body|string|true|Updated due date of the item|

<h3 id="additemwithform-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|Invalid input|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteItem

<a id="opIddeleteItem"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId} \
  -H 'api_key: string'

```

```http
DELETE https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId} HTTP/1.1
Host: virtserver.swaggerhub.com

api_key: string

```

```javascript

const headers = {
  'api_key':'string'
};

fetch('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'api_key' => 'string'
}

result = RestClient.delete 'https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'api_key': 'string'
}

r = requests.delete('https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'api_key' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "api_key": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://virtserver.swaggerhub.com/SANIYAAHUJA/ToDo/1.0.0/Items/deleteItem/{itemId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /Items/deleteItem/{itemId}`

*Deletes an item*

<h3 id="deleteitem-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|api_key|header|string|false|none|
|itemId|path|integer(int64)|true|Item to delete|

<h3 id="deleteitem-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Invalid ID supplied|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Item not found|None|

<aside class="success">
This operation does not require authentication
</aside>

