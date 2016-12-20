## base
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


## account
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|Account Name| `base/name` |  |
|id|Account ID| `base/uuid` |  |


## author
| Id | Info | Type | Schema |
|----|------|------|--------|
|info|Author of the change| `` |  |


## user
| Id | Info | Type | Schema |
|----|------|------|--------|
|name|User's full name| `base/name` |  |
|id|User ID| `base/uuid` |  |
|email|User email| `base/email` |  |


