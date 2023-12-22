# 箱门控制

## 方法

## `openBoxDoor(doorIds, mode) → {Promise.<boolean>}`

打开箱门

### 参数

| 名称      | 类型     | 必填 | 说明                                      |
| --------- | -------- | ---- | ----------------------------------------- |
| `doorIds` | number[] | 是   | 箱门号列表，取值范围：1~4。               |
| `mode`    | number   | 否   | 执行端模式：1=上位机，2=底盘；默认值：1。 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
// 打开1号箱门
const success = await axRobot.openBoxDoor([1], 1);
...
```



## `closeBoxDoor(doorIds, mode) → {Promise.<boolean>}`

关闭箱门

### 参数

| 名称      | 类型     | 必填 | 说明                                      |
| --------- | -------- | ---- | ----------------------------------------- |
| `doorIds` | number[] | 是   | 箱门号列表，取值范围：1~4。               |
| `mode`    | number   | 否   | 执行端模式：1=上位机，2=底盘；默认值：1。 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```javascript
...
// 关闭2号箱门
const success = await axRobot.closeBoxDoor([2], 1);
...
```