# 暂停任务列表分配任务

## 方法

## `pauseQueue(key) -> {Promise.<boolean>}`

请求成功后，指定的队列将暂停分配任务。主要用于后台管理和设置整个队列任务排序时

### 参数

| 名称   | 类型                          | 说明     |
| ------ | ----------------------------- | -------- |
| `key` | string | 队列标识，业务标识或机器人标识 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.pauseQueue(key);
...
```



