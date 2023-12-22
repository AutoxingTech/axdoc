# Edit Map

## `clearAreaMap() -> {void}`

Clear area map

### Parameters

none

### Return Value

none

### Example

```javascript
...
axMap.clearAreaMap();
...
```

## `clearFeature() -> {void}`

Clear map data

### Parameters

none

### Return Value

none

### Example

```javascript
...
axMap.clearFeature();
...
```

## `deleteFeature(id) -> {void}`

deletes the specified feature

### Parameters

| Name | Data Type | Description |
| ---- | -------- | ------------ |
| `id` | string | feature identifier |

### Return Value

none

### Example

```javascript
...
axMap.deleteFeature("<featureId>");
...
```

## `editPose(coordinates, properties opt) -> {void}`

Set the current point pose

### Parameters

| Name | Data Type | Description |
| -------------- | ------------- | ---------------- |
| `coordinates` | array<number> | coordinates [x, y] Unit: meters|
| `properties` | object | optional; custom properties |

### Return Value

none

### Example

```javascript
...
axMap.editPose([0, 0]);
...
```

## `endEditPose() -> {object}`

Cancel the current point pose

### Parameters

none

### Return Value `object`

Edited pose

### Example

```javascript
...
const post = axMap.endEditPose();
...
```
