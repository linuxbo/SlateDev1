---
title: Alpaca API Reference

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Alpaca API! Did you know that Alpacas make a bvvt sound!? You can use our API to access Alpaca API endpoints, which can get information on various Alpacas in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'alpaca'

api = Alpaca::APIClient.authorize!('bvvtbvvtbvvt')
```

```python
import Alpaca

api = Alpaca.authorize('bvvtbvvtbvvt')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: bvvtbvvtbvvt"
```

```javascript
const alpaca = require('alpaca');

let api = alpaca.authorize('bvvtbvvtbvvt');
```

> Make sure to replace `bvvtbvvtbvvt` with your API key. [I have already done so, as the API key is now bvvt instead of meow]

Alpaca uses API keys to allow access to the API. You can register a new Alpaca API key at our [developer portal](http://Alpaca.com/developers).

Alpaca expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: bvvtbvvtbvvt`

<aside class="notice">
You may replace <code>bvvtbvvtbvvt</code> with your personal API key, however I would not suggest it.
</aside>

# Alpaca

## Get All Alpaca

```ruby
require 'alpaca'

api = Alpaca::APIClient.authorize!('bvvtbvvtbvvt')
api.alpaca.get
```

```python
import alpaca

api = alpaca.authorize('bvvtbvvtbvvt')
api.alpaca.get()
```

```shell
curl "http://alpaca.com/api/alpaca"
  -H "Authorization: bvvtbvvtbvvt"
```

```javascript
const alpaca = require('alpaca');

let api = alpaca.authorize('bvvtbvvtbvvt');
let kittens = api.alpaca.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Bailey",
    "breed": "Huacaya",
    "fluffiness": 10,
    "cuteness": 10
  },
  {
    "id": 2,
    "name": "Elwen",
    "breed": "Huacaya",
    "fluffiness": 10,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Alpacas.

### HTTP Request

`GET http://example.com/api/alpacas`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve
