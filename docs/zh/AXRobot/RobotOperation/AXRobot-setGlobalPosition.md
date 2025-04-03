# 设置全局定位

## `setGlobalPosition() -> {Promise.<boolean>}`

设置机器人全局位置

### 参数

无

### 返回值 `Promise.<boolean>`

设置是否可信

* `true` - 可信
* `false` - 不可信

### 示例

```typescript
...
const success = await axRobot.setGlobalPosition();
...
```

