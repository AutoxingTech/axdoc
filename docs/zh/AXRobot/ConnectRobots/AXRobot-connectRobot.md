# 连接

## `connectRobot(req) -> {Promise}`

连接机器人

### 参数

| 名称  | 数据类型   | 说明     |
| ----- | ---------- | -------- |
| `req` | ReqConnect | 连接参数 |

### 返回值 `Promise`

无

### 示例

```typescript
// 初始化机器人操作实例
...
try {
  const res = await axRobot.connectRobot({
    robotId: "<robotId>"
  });
  
  console.log("connect success: " + res.robotId);
  // do something
} catch(err) {
  console.log(err.errText);
}
```

