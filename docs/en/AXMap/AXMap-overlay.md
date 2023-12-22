# Overlay Operation

## `addPoint(coordinates, properties opt) -> {string}`

Add points to the map

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ---------------- |
| `coordinates` | number[] | point coordinates [x, y] Unit: meters|
| `properties` | object | optional; custom properties |

### Return value `string`

feature identifier of the added point

### Example

```javascript
...
axMap.addPoint([0, 0], {
  name: "test", // name
  color: "#f00", // color
  radius: 2, // radius, unit: pixel
  yaw: 0, // facing angle
  enableSelect: true // whether to allow selection
});
...
```

## `addLine(coordinates, properties opt) -> {string}`

Add lines to the map

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ---------------- |
| `coordinates` | array[] | array of point coordinates on the line Unit: meters|
| `properties` | object | optional; custom properties |

### Return value `string`

The feature ID of the added line

### Example

```javascript
...
axMap.addLine([[0, 0], [10, 10], {
  color: "#f00", // color
  width: 2, // width, unit: pixel
  dash: 'dash' // dashed line
});
...
```

## `addMarker(imgSrc, coordinates, yaw) -> {any}`

Add a marker to the map

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ----------- |
| `imgSrc` | string | Image address |
| `coordinates` | number[] | coordinates [x, y] Unit: meters|
| `yaw` | number | facing angle Unit: degrees|

### Return value `any`

marker object

### Example

```javascript
...
const marker = axMap.addMarker("<imgSrc>", [0, 0], 0);
...
```

## `setMarkerProperties(marker, coordinates, yaw) -> {void}`

Set marker properties

### Parameters

| Name | Data Type | Description |
| ------------- | -------- | ------------- |
| `marker` | any | marker object |
| `coordinates` | number[] | new coordinates [x, y] Unit: meters|
| `yaw` | number | new heading angle Unit: degrees|

### return value

none

### Example

```javascript
...
axMap.setMarkerProperties(marker, [1, 1], 0);
...
```

## `removeMarker(marker) -> {void}`

remove marker from map

### Parameters

| Name | Data Type | Description |
| -------- | -------- | ------------- |
| `marker` | any | Marker object |

### return value

none

### Example

```javascript
...
axMap.removeMarker(marker);
...
```
