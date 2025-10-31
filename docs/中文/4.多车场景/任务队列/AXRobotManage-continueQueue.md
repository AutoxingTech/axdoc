# 继续任务列表分配任务

## 方法

## `continueQueue(key) -> {Promise.<boolean>}`

请求成功后，指定的任务队列将继续分配任务。用于后台管理和设置完整个队列排序后

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
const success = await axRobot.continueQueue(key);
...
```



