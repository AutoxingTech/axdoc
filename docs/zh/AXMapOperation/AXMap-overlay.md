# 叠加物操作

## `addPoint(coordinates, properties opt) -> {string}`

向地图中添加点

### 参数

| 名称          | 数据类型 | 说明             |
| ------------- | -------- | ---------------- |
| `coordinates` | number[] | 点坐标 [x, y]  单位:米|
| `properties`  | object   | 可选；自定义属性 |

### 返回值 `string`

添加点的 feature 标识

### 示例

```typescript
...
axMap.addPoint([0, 0], {
  name: "test", // 名称
  color: "#f00", // 颜色
  radius: 2, // 半径，单位：像素
  yaw: 0, // 朝向角度
  enableSelect: true // 是否允许选择
});
...
```

## `addLine(coordinates, properties opt) -> {string}`

向地图中添加线

### 参数

| 名称          | 数据类型 | 说明             |
| ------------- | -------- | ---------------- |
| `coordinates` | array[]  | 线上的点坐标数组 单位:米|
| `properties`  | object   | 可选；自定义属性 |

### 返回值 `string`

添加线的 feature 标识

### 示例

```typescript
...
axMap.addLine([[0, 0], [10, 10], {
  color: "#f00", // 颜色
  width: 2, // 宽度，单位：像素
  dash: 'dash' // 虚线
});
...
```

## `addMarker(imgSrc, coordinates, yaw) -> {any}`

向地图中添加 marker

### 参数

| 名称          | 数据类型 | 说明        |
| ------------- | -------- | ----------- |
| `imgSrc`      | string   | 图片地址    |
| `coordinates` | number[] | 坐标 [x, y] 单位:米|
| `yaw`         | number   | 朝向角度    单位:度|

### 返回值 `any`

marker 对象

### 示例

```typescript
...
const marker = axMap.addMarker("<imgSrc>", [0, 0], 0);
...
```

## `setMarkerProperties(marker, coordinates, yaw) -> {void}`

设置 marker 属性

### 参数

| 名称          | 数据类型 | 说明          |
| ------------- | -------- | ------------- |
| `marker`      | any      | marker 对象   |
| `coordinates` | number[] | 新坐标 [x, y] 单位:米|
| `yaw`         | number   | 新的朝向角度  单位:度|

### 返回值

无

### 示例

```typescript
...
axMap.setMarkerProperties(marker, [1, 1], 0);
...
```

## `removeMarker(marker) -> {void}`

从地图中删除 marker

### 参数

| 名称     | 数据类型 | 说明        |
| -------- | -------- | ----------- |
| `marker` | any      | Marker 对象 |

### 返回值

无

### 示例

```typescript
...
axMap.removeMarker(marker);
...
```

