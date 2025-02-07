# hashcash-256 JS

experimental sha256 implementation of hashcash

## Install

`npm install okyanusoz/hashcash-js`

or

`yarn add okyanusoz/hashcash-js`

## Usage

```js
import Hashcash from 'hashcash-sha256'
```

### Generating a stamp

```js
const stamp = Hashcash.generateStamp(16, "unique-data-goes-here")
console.log(stamp)
```

Would output something like the following (except the trail):

```
1:16:20180708232351:unique-data-goes-here::xDnc81q
```

## Assumptions

In this implementation we've used HHMMSS on the timestamp, instead of the original date-only approach.  This gives more flexibility to the receiving side for strict checking per minute, second, hour, etc.  Changing this precision may be an option in future releases.
