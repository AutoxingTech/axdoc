# 获取网络模式

## `getRouteMode() -> {Promise.<string>}`

获取机器人网络模式

### 参数

无

### 返回值 `Promise.<string>`

网络模式

### 示例

```typescript
const mode = await axRobot.getRouteMode();
console.log(mode); 
```

> * **说明：** 返回值：etho_first: "头壳WIFI供网"/"头壳4G供网"(可根据头壳是否连接wifi,自行判断), wlan0_first: "底盘WIFI供网", usbo_first: "底盘4G供网"

