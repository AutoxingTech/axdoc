# Sprayer Control

## Methods

## `openSprayer(gear) → {Promise.<boolean>}`

Turn on the sprayer

### Parameters

| Name | Type | Description |
| ------ | ------ | ---- |
| `gear` | number | gear |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.openSprayer("<gear>");
...
```



## `closeSprayer() → {Promise.<boolean>}`

Turn off the sprayer

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
const success = await axRobot.closeSprayer();
...
```
