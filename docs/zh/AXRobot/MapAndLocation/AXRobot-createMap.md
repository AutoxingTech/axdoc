# 创建地图

## `createMap(containerId, backgroundColor opt) -> {Promise.<AXMap>}`

创建地图

### 参数

| 名称              | 数据类型 | 说明                        | 备注                                                                                           |
| ----------------- | -------- | --------------------------- | ---------------------------------------------------------------------------------------------- |
| `containerId`     | string   | 地图的显示容器 HTML 标签 ID |                                                                                                |
| `backgroundColor` | string   | 可选；地图背景色            |                                                                                                |
| `glyphs`          | string   | 可选；地图字体库            | 1：在 web 端使用，可以使用 http、https 或者相对路径<br/>2：非 web 端，必须使用 http 或者 https |

### 返回值 `Promise.<AXMap>`

地图实例

### 示例

```typescript
...
const map = await axRobot.createMap("map", "#eeeeee");
...
```
