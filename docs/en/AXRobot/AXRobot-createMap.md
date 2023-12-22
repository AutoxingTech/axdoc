# Create Map

## `createMap(containerId, backgroundColor opt) -> {Promise.<AXMap>}`

Create a map

### Parameters

| Name | Data Type | Description |
| ----------------- | -------- | --------------------------- |
| `containerId` | string | HTML tag ID of the display container for the map |
| `backgroundColor` | string | optional; map background color |
| `glyphs`          | string   | optional; map fonts            | 1: Use on the web side, you can use http, https or relative path<br/>2: Non-web side, you must use http or https |

### Return value `Promise.<AXMap>`

map instance

### Example

```javascript
...
const map = await axRobot.createMap("map", "#eeeeee");
... 
```
