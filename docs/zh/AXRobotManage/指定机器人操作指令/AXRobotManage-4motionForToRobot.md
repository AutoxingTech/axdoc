# 指定机器人运动控制
## 方法

## `motionForToRobot(type, robotId） -> {Promise.<boolean>}`

SDK无需连接机器人，通过该方法可实现对指定的某个机器人进行控制。

### 参数

| 名称       | 类型                                         | 说明         |
| --------- | -----------------------------                | ------------ |
| `type`    | [MotionType](../../Define/Define-MotionType) | 运动方式      |
| `robotId` | number                                       | 机器人标识    |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.motionForToRobot(MotionType.Forward, robotId);
...
```



