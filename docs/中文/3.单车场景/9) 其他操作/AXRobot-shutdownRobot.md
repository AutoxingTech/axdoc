# 机器人关机

## `shutdownRobot() -> {Promise.<boolean>}`

重新启动机器人

### 参数

无

### 返回值 `Promise.<boolean>`

设置是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
const success = await axRobot.shutdownRobot();
...
```

