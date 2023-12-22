# 其他

## `beautifyMapImg(imgUrl, obstacle, throughArea, other) -> {Promise.<string>}`

美化地图图片

### 参数

| 名称          | 数据类型 | 说明                                                       |
| ------------- | -------- | ---------------------------------------------------------- |
| `imgUrl`      | string   | 源图片地址                                                 |
| `obstacle`    | object   | 障碍物 RGBA颜色值<br/>示例：`{r: 42, g:124, b:128, a:255}` |
| `throughArea` | object   | 可通行区载 RGBA 颜色值                                     |
| `other`       | object   | 其他区域 RGBA 颜色值                                       |

### 返回值 `Promise.<string>`

美化后的图片地址

### 示例

```typescript
...
const newImg = await axMap.beautifyMapImg("<imgUrl>", {...}, {...}, {...});
...
```

## `project(coordinates) -> {array.<number>}`

将地图坐标转换为像素偏移

### 参数

| 名称          | 数据类型      | 说明            |
| ------------- | ------------- | --------------- |
| `coordinates` | array<number> | 地图坐标 [x, y] |

### 返回值 `array.<number>`

转换后的像素偏移

### 示例

```typescript
...
const pixel = axMap.project([0, 0]);
...
```

## `destroy() -> {void}`

销毁地图对象

### 参数

无

### 返回值

无

### 示例

```typescript
...
axMap.destroy();
...
```

