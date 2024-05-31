# 指定机器人恢复任务
## 方法

## `resumeTaskToRobot(robotId） -> {Promise.<boolean>}`

SDK无需连接机器人，通过该方法可实现对指定的某个机器人恢复任务

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `robotId` | string | 机器人标识 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.resumeTaskToRobot(robotId）;
...
```



