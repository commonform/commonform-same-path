check whether two Common Form paths are the same

```javascript
var assert = require('assert')
var samePath = require('commonform-same-path')

assert.strictEqual(
  samePath(['content', 0], ['content', 0]),
  true
)

assert.strictEqual(
  samePath(['content', 0], ['content', 1]),
  false
)

assert.throws(function () {
  samePath('not an array', ['content', 1])
})

assert.throws(function () {
  samePath(['content', 1], 'not an array')
})
```
