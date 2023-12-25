# Light Belt Control

## Methods

## `openLightBelt(lightBelt) → {Promise.<boolean>}`

Turn on the light strip

### Parameters

| Name | Type | Description |
| ----------- | ------------------------------- | ---- |
| `lightBelt` | [LightBelt](../../../Define/Define-LightBelt) |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
let lightBelt = {
  mode: 1,
  color: LightColor.Green,
  indexes: [
    { index: 0, num: 6 }
  ]
}
const success = await axRobot.openLightBelt(lightBelt);
...
```



## `closeLightBelt(lightBelt) → {Promise.<boolean>}`

Turn off the light strip

### Parameters

| Name | Type | Description |
| ----------- | ------------------------------- | ---- |
| `lightBelt` | [LightBelt](../../Define/Define-LightBelt) |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```javascript
...
let lightBelt = {
mode: 1,
  color: LightColor.Green,
indexes: [
    { index: 0, num: 6 }
  ]
}
const success = await axRobot.closeLightBelt(lightBelt);
...
```
