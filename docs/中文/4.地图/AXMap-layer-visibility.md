# 地图图层显隐

## `setBackCustomImg(img) -> {void}`

设置自定义背景图片

### 参数

| 名称 | 数据类型 | 说明 |
| ---- | -------- | ---- |
| `img` | string/Image | 图片地址或图片对象 |

### 返回值

无

### 示例

```typescript
...
const img = require('./6.png')
await axMap.setBackCustomImg(img)
...
```

## `showMapImgLayer(visible) -> {Promise<void>}`

设置地图层显隐

### 参数

| 名称 | 数据类型 | 说明 |
| ---- | -------- | ---- |
| `visible` | boolean | true 显示，false 隐藏 |

### 返回值

Promise<void>

### 示例

```typescript
...
// 隐藏地图层
await axMap.showMapImgLayer(false)
// 显示地图层
await axMap.showMapImgLayer(true)
...
```

## `showLineStringLayer(visible) -> {Promise<void>}`

设置路线层显隐

### 参数

| 名称 | 数据类型 | 说明 |
| ---- | -------- | ---- |
| `visible` | boolean | true 显示，false 隐藏 |

### 返回值

Promise<void>

### 示例

```typescript
...
// 隐藏路线层
await axMap.showLineStringLayer(false)
// 显示路线层
await axMap.showLineStringLayer(true)
...
```

## `showPointLayer(visible) -> {Promise<void>}`

设置点位层显隐

### 参数

| 名称 | 数据类型 | 说明 |
| ---- | -------- | ---- |
| `visible` | boolean | true 显示，false 隐藏 |

### 返回值

Promise<void>

### 示例

```typescript
...
// 隐藏点位层
await axMap.showPointLayer(false)
// 显示点位层
await axMap.showPointLayer(true)
...
```
