# 地图交互

## `setAreaMap(areaId) -> {void}`

设置区域地图

### 参数

| 名称     | 数据类型 | 说明         |
| -------- | -------- | ------------ |
| `areaId` | string   | 地图区域标识 |

### 返回值

无

### 示例

```typescript
...
axMap.setAreaMap("<areaId>");
...
```

## `setMapCenter(coordinates) -> {void}`

设置地图中心点

### 参数

| 名称          | 数据类型      | 说明              |
| ------------- | ------------- | ----------------- |
| `coordinates` | array<number> | 中心点坐标 [x, y] |

### 返回值

无

### 示例

```typescript
...
axMap.setMapCenter([0, 0]);
...
```

## `zoomTo(zoom) -> {void}`

设置地图缩放级别

### 参数

| 名称   | 数据类型 | 说明                        |
| ------ | -------- | --------------------------- |
| `zoom` | number   | 地图缩放级别，取值范围 0~22 |

### 返回值

无

### 示例

```typescript
...
axMap.zoomTo(10);
...
```

## `fly(coordinates) -> {void}`

地图飞至某点

### 参数

| 名称          | 数据类型      | 说明              |
| ------------- | ------------- | ----------------- |
| `coordinates` | array<number> | 目标点坐标 [x, y] |

### 返回值

无

### 示例

```typescript
...
axMap.fly([0, 0]);
...
```

## `getCurrentPointPosition(featureId) -> {object}`

获取当前选中点位姿

### 参数

| 名称        | 数据类型 | 说明   |
| ----------- | -------- | ------ |
| `featureId` | string   | 点标识 |

### 返回值 `object`

位姿信息

* `x` - 坐标 x 分量
* `y` - 坐标 y 分量
* `yaw` - 朝向角

### 示例

```typescript
...
const pose = axMap.getCurrentPointPosition("<featureId>");

console.log(pose); // {x:1, y: 2, yaw: 3}
...
```

## `getFeature(id) -> {object}`

根据标识获取 feature 信息

### 参数

| 名称 | 数据类型 | 说明         |
| ---- | -------- | ------------ |
| `id` | string   | feature 标识 |

### 返回值 `object`

feature 信息；结构参考 [https://geojson.org/](https://geojson.org/)

### 示例

```typescript
...
const feature = axMap.getFeature("<featureId>");
...
```

## `getPlaceList() -> {any}`

获取所有位置点

### 参数

无

### 返回值 `any`

位置点列表；结构参考 [https://geojson.org/](https://geojson.org/)

### 示例

```typescript
...
const list = axMap.getPlaceList();
...
```

## `setClickMapCallback(callback) -> {void}`

设置点击地图回调方法

### 参数

| 名称       | 数据类型 | 说明     |
| ---------- | -------- | -------- |
| `callback` | function | 回调方法 |

### 返回值

无

### 示例

```typescript
...
axMap.setClickMapCallback(val => {
  console.log(val.type); // 固定为 'LayerPoint'
  console.log(val.data); // 被点击的元素，数据结构参考 GeoJSON
});
...
```

## `setSelectedFeatures(featureId) -> {void}`

根据标识选中地图中的 feature

### 参数

| 名称        | 数据类型 | 说明                                      |
| ----------- | -------- | ----------------------------------------- |
| `featureId` | string   | feature 标识，多个 feature 标识用逗号分隔 |

### 返回值

无

### 示例

```typescript
...
axMap.setSelectedFeatures("<featureId>");
...
```

