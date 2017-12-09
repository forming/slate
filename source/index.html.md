---
title: API Reference

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

## What is Phore?

Phore is a digital privacy cryptocurrency with a focus on sustainable development and growth. Phore uses Proof of Stake and Masternodes to secure the network and provide for a deep level of privacy and security. Phore has relatively fast block times compared with Bitcoin and low transaction fees. 

## Coin Information

 | 
--------- |
Block Target: 60 seconds |
Transaction Fee: 0.0001 PHR per kB |

## History

Phore is a digital privacy cryptocurrency, an update and rebrand of KryptKoin (KTK) which was
pre-announced in May 2014, and whose distribution started on the 21st May 2014.
Kryptkoin was a non-premined coin, distributed equally to people who qualified for a stake. In
total, 500 stakes were distributed in 2 stages. Bonus KTK was given to those who held for 30
days. There was no ICO, and no dev premine. The developer received 1 stake, the same as
every other stakeholder received. Following launch, Kryptkoin quickly developed a large
following and introduced an online marketplace in 2015, which included Paypal integration
where digital items such as Wordpress themes and physical items such as clothes were both
listed and bought.
To facilitate new features, the existing code needed to be rewritten from scratch. This required
a swap from Kryptkoin to the new Phore.
A two-month window was given to existing KTK holders to swap their coins for new Phore on a
1:1 basis.

## Team

The coin has a strong and committed team:
    ● Phroshi - Lead Developer
    ● Julian - Core Developer
    ● Fish313 - Technical Support & Social Media Manager
    ● Toby - Customer Relations & Social Media Manager
    ● Shanto - Community Manager & Customer Relations
    ● Liray - Technical Support & Japanese Community Manager
    ● Ubermaster - Planning and Partnerships

We will hire more staff and developers to strengthen our team as the Phore expands and
evolves.

## Roadmap

Phore is a restless currency.
The key challenge going forward is to introduce real-world use which attract everyday
people. In order to achieve this, Phore will implement advanced features to clearly differentiate
Phore from other privacy based digital currencies.
A number of these will add to the functionality and strategic integration of the online
marketplace, which will be built on the current foundations of Phore.
Governance will determine many of the goals going forward to keep the currency decentralized, but a decrease in Master node rewards per block is expected to decrease
inflation.

## Short Term (Q3 - Q4, 2017)

    ● Masternode Governance - Those with Masternodes would be given ‘yes’ or ‘no’ votes
    using commands built into Phore wallets. Decentralized governance will allow a cryptocurrency
    network to grow, and incorporate democratic procedures that will ensure the
    longevity of the project, leading to a truly decentralized management system.
    ● Online Marketplace - UI compatibility for all devices. 

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

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

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

