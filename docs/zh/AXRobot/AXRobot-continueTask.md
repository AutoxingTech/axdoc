# 继续任务

## 方法

## `continueTask() -> {Promise.<boolean>}`

继续正在执行的任务（主要针对人机交互动作而暂停的任务）。

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.continueTask();
...
```



