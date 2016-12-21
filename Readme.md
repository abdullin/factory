## factory

Factory information

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|Factory name| `base/name` |  |
|id|Factory id| `base/uuid` |  |


## shelf

A shelf in a rack

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|code|Shelf code| `base/code` |  |
|id|Shelf id| `base/uuid` |  |


## author

Authoring information

### Type info
Author of the change

 * account/id
 * user/id

## user

User information

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|User's full name| `base/name` |  |
|id|User ID| `base/uuid` |  |
|email|User email| `base/email` |  |


## base

Base values and native aliases

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|char6|Characters in [a-zA-Z0-9_\.], can git in 6 bits| `native/string` |  |
|string|Simple string| `native/string` |  |
|name|A single line that code be dsiplayed| `base/string` | `((limit 1 128))` |
|id|Positive id| `base/uint64` |  |
|code|Non-empty identifier| `base/char6` | `((limit 1 64))` |
|line|One line of a unicode text| `base/string` |  |
|token|Author's access token| `base/string` |  |
|uuid|Unique id, monotonically increasing| `native/uuid` |  |
|text|Multiple lines of unicode text| `base/string` |  |
|sku|Product SKU code| `base/char6` | `((limit 4 64))` |
|email|A valid email| `base/string` | `((limit 5 128))` |
|uint64|Positive 64 bit number| `native/uint64` |  |


## product

Finished good

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|Description| `base/text` | `((limit 0 1024))` |
|id|UUID for the product id| `base/uuid` |  |


## geo

Types and specs for assigning things to geo position

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|lon|Longtitude| `native/float64` |  |
|lat|Latitude| `native/float64` |  |


### Type point
Geographical location

 * lat
 * lon

## address

Shipping information

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|Persons name| `base/line` | `((limit 0 128))` |
|city|City name| `base/line` | `((limit 0 64))` |
|state|State or province| `base/line` | `((limit 0 32))` |
|postal|Postal code see [Wiki](https://en.wikipedia.org/wiki/Postal_code) | `base/line` | `((limit 0 10))` |
|line2|Line 2 of the address| `base/line` | `((limit 0 128))` |
|line1|Line 1 of the address| `base/line` | `((limit 1 128))` |
|country|Country code| `base/char6` | `((limit 2 2))` |


### Type address
Address that could be used for shipping or billing

 * name
 * line1
 * line2
 * country
 * postal
 * city
 * state

## account

Account information

### Specs
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|Account Name| `base/name` |  |
|id|Account ID| `base/uuid` |  |


