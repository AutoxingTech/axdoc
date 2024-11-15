# 重新开始任务

## 方法

## `restartTask(taskId) -> {Promise.<boolean>}`

重新开始已暂停或结束的任务。

### 参数

| 名称     | 类型   | 说明     |
| -------- | ------ | -------- |
| `taskId` | string | 任务标识 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.restartTask("<taskId>");
...
```



