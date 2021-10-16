# @mf3rnol/dynamic-forward-proxy

[![NPM Version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]
[![Downloads Stats][npm-downloads]][npm-url]

> WIP

Set of services for maintaining a list of proxies and their performance metrics.
Includes a forward-proxy server that works with the pool once established, and a
bot to control opertation and create custom sub-pools for individuual
users/user-cases

#### Updating the GeoIP Lite DB

If desired, the included GeoIP lite database may e updated via:

```bash
npm run update-geoip-db
```

### [Release History](#release_history)

See *[CHANGELOG.md](CHANGELOG.md)* for more information.

### [License](#license)

Distributed under the **MIT** license. See [LICENSE.md](LICENSE.md) for more information.

### [Contributing](#contributing)

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

---

<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/proxy-evaluator.svg?style=flat-square
[npm-url]: https://npmjs.org/package/proxy-evaluator
[npm-downloads]: https://img.shields.io/npm/dm/proxy-evaluator.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/mf3rnol/proxy-evaluator/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/mf3rnol/proxy-evaluator

---

## [API Reference](#api_reference)

> The standalone JSDoc reference can be found in [DOCUMENTATION.md](DOCUMENTATION.md)

## Functions

<dl>
<dt><a href="#parse">parse(proxyString, protocol)</a> ⇒ <code>object</code></dt>
<dd></dd>
<dt><a href="#createBot">createBot(token)</a> ⇒ <code>TelegramBot</code></dt>
<dd><p>Returns a TG bot instance.</p>
</dd>
<dt><a href="#createEnum">createEnum(values)</a> ⇒ <code><a href="#Enum">Enum</a></code></dt>
<dd><p>Returns a <strong>frozen</strong> object with the provided string values set as uppercase
keys mapped to unique numeric IDs. Entries are trimmed for whitespace.</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#Enum">Enum</a></dt>
<dd><p>Enum implementation; a frozen object with uppercase keys mapping to unique
numeric IDs.</p>
</dd>
</dl>

<a name="parse"></a>

## parse(proxyString, protocol) ⇒ <code>object</code>
**Kind**: global function  
**Todo**

- [ ] add typedef for returned proxy [info] object


| Param | Type | Description |
| --- | --- | --- |
| proxyString | <code>string</code> | may include protocol as prefix |
| protocol | <code>string</code> | http, https, socks4, socks5 |

<a name="createBot"></a>

## createBot(token) ⇒ <code>TelegramBot</code>
Returns a TG bot instance.

**Kind**: global function  
**Returns**: <code>TelegramBot</code> - bot  
**Todo**

- [ ] improve description
- [ ] Switch to web-hook connection immediately


| Param | Type | Description |
| --- | --- | --- |
| token | <code>string</code> | TG bot API token |

<a name="createEnum"></a>

## createEnum(values) ⇒ [<code>Enum</code>](#Enum)
Returns a **frozen** object with the provided string values set as uppercase
keys mapped to unique numeric IDs. Entries are trimmed for whitespace.

**Kind**: global function  
**Returns**: [<code>Enum</code>](#Enum) - e  
**Throws**:

- Error if passed a non-array or no values

**Todo**

- [ ] use custom error objects


| Param | Type | Description |
| --- | --- | --- |
| values | <code>Array.&lt;string&gt;</code> | e values, converted to uppercase keys on the   rseulting object |

<a name="Enum"></a>

## Enum
Enum implementation; a frozen object with uppercase keys mapping to unique
numeric IDs.

**Kind**: global typedef  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| [size] | <code>number</code> | <code>2</code> | number of entries |
| toString | <code>function</code> |  | returns a string with all e keys |
| includes | <code>function</code> |  | takes a value and returns true if the e   contains it as an entry. |


