# 取消任务

## 方法

## `cancelTask() -> {Promise.<boolean>}`

取消当前正在执行的任务。

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.cancelTask();
...
```



