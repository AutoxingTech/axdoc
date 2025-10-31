# 设置网络模式

## `setRouteMode(mode) -> {Promise.<boolean>}`

设置机器人上网模式

### 参数

| 名称   | 类型   | 说明                     |
| ------ | ------ | ------------------------ |
| `mode` | number | 网络类型<br/> 0: 头壳供网<br/> 1: 底盘wifi供网<br/> 2: 底盘4G供网<br/> 3: 底盘供网 |

### 返回值 `Promise.<boolean>`

是否成功

* true - 成功
* false - 失败

### 示例

```typescript
...
const success = await axRobot.setRouteMode(0);
...
```

