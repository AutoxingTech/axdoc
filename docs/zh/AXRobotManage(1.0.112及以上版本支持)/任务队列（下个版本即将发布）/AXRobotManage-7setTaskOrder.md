# 设置单个任务在队列中的顺序

## 方法

## `setTaskOrder(taskSn, refTaskSn, isFront) -> {Promise.<boolean>}`

开始执行任务。

### 参数

| 名称         | 类型                    | 说明                           |
| --------- | ---------------------- | ------------------                        |
| `taskSn`     | string                 | 要设置排序的任务 SN                      |
| `refTaskSn`  | string                 | 指代的任务排序将移动到此任务的前面或后面      |
| `isFront`    | boolean                | 是否移动到前面  默认为 false，会移动到参考任务的后面    |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
const success = await axRobot.setTaskOrder(taskSn, refTaskSn, isFront);
...
```



