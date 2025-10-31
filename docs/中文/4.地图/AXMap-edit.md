# 地图编辑

## `clearAreaMap() -> {void}`

清除区域地图

### 参数

无

### 返回值

无

### 示例

```typescript
...
axMap.clearAreaMap();
...
```

## `clearFeature() -> {void}`

清空地图数据

### 参数

无

### 返回值

无

### 示例

```typescript
...
axMap.clearFeature();
...
```

## `deleteFeature(id) -> {void}`

删除指定标识的 feature

### 参数

| 名称 | 数据类型 | 说明         |
| ---- | -------- | ------------ |
| `id` | string   | feature 标识 |

### 返回值

无

### 示例

```typescript
...
axMap.deleteFeature("<featureId>");
...
```

## `editPose(coordinates, properties opt) -> {void}`

设置当前点位姿

### 参数

| 名称           | 数据类型      | 说明             |
| -------------- | ------------- | ---------------- |
| `coordinates` | array<number> | 坐标 [x, y]    单位:米  |
| `properties`   | object        | 可选；自定义属性 |

### 返回值

无

### 示例

```typescript
...
axMap.editPose([0, 0]);
...
```

## `endEditPose() -> {object}`

取消设置当前点位姿

### 参数

无

### 返回值 `object`

编辑后的位姿

### 示例

```typescript
...
const post = axMap.endEditPose();
...
```

