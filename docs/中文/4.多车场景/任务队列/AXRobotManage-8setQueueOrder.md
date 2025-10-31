# 设置整个任务队列排序

## 方法

## `setQueueOrder(key, newOrder) -> {Promise.<boolean>}`

开始执行任务。

### 参数

| 名称      | 类型                    | 说明                    |
| --------- | ---------------------- | ------------------      |
| `key`     | string                 | 队列标识，业务标识或机器人标识 |
| `newOrder`| Array<string>          | 任务队列新排序      |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.setQueueOrder(key, ["string", "string"]);
...
```



