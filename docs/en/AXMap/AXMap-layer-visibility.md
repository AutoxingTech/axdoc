# Map Layer Visibility

## `setBackCustomImg(img) -> {void}`

Set custom background image

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ---- |
| `img` | string/Image | Image address or image object |

### Return value

none

### Example

```javascript
...
const img = require('./6.png')
await axMap.setBackCustomImg(img)
...
```

## `showMapImgLayer(visible) -> {Promise<void>}`

Set map layer visibility

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ---- |
| `visible` | boolean | true to show, false to hide |

### Return value

Promise<void>

### Example

```javascript
...
// Hide map layer
await axMap.showMapImgLayer(false)
// Show map layer
await axMap.showMapImgLayer(true)
...
```

## `showLineStringLayer(visible) -> {Promise<void>}`

Set line layer visibility

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ---- |
| `visible` | boolean | true to show, false to hide |

### Return value

Promise<void>

### Example

```javascript
...
// Hide line layer
await axMap.showLineStringLayer(false)
// Show line layer
await axMap.showLineStringLayer(true)
...
```

## `showPointLayer(visible) -> {Promise<void>}`

Set point layer visibility

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ---- |
| `visible` | boolean | true to show, false to hide |

### Return value

Promise<void>

### Example

```javascript
...
// Hide point layer
await axMap.showPointLayer(false)
// Show point layer
await axMap.showPointLayer(true)
...
```
