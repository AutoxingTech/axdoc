# 更新任务

## `updateTask(taskId, pts) -> {Promise.<boolean>}`

更新任务。

### 参数

| 名称     | 类型   | 说明                                          |
| -------- | ------ | --------------------------------------------- |
| `taskId` | string | 任务标识                                      |
| `pts`    | Array  | 任务点列表；参考开始执行任务的 `taskPts` 参数 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...

const success = await axRobot.updateTask("<taskId>", <pts>);
...
```
