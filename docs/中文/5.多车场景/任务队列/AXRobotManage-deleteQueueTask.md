# 删除指定任务

## 方法

## `deleteQueueTask(taskSn) -> {Promise.<boolean>}`

任务只有在分配状态下才可以删除

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `taskSn` | string | 任务记录 SN |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.deleteQueueTask(taskSn);
...
```



