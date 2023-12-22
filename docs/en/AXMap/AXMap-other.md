# Others

## `beautifyMapImg(imgUrl, obstacle, throughArea, other) -> {Promise.<string>}`

Beautify the map picture

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ------------------------------------------------------------ |
| `imgUrl` | string | Source image address |
| `obstacle` | object | Obstacle RGBA color value<br/>Example: `{r: 42, g:124, b:128, a:255}` |
| `throughArea` | object | Passable area load RGBA color value |
| `other` | object | other area RGBA color value |

### Return Value `Promise.<string>`

The beautified image address

### Example

```javascript
...
const newImg = await axMap.beautifyMapImg("<imgUrl>", {...}, {...}, {...});
...
```

## `project(coordinates) -> {array.<number>}`

Convert map coordinates to pixel offsets

### Parameters

| Name | Data Type | Description |
| ------------- | ------------- | --------------- |
| `coordinates` | array<number> | map coordinates [x, y] Unit: meters|

### Return Value `array.<number>`

Converted pixel offset

### Example

```javascript
...
const pixel = axMap.project([0, 0]);
...
```

## `destroy() -> {void}`

destroy map object

### Parameters

none

### Return Value

none

### Example

```javascript
...
axMap.destroy();
...
```
