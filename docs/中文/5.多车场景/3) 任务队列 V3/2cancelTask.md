# 取消任务

## 方法

## `cancelTaskV3(taskId) -> {Promise.<Boolean>}`

根据业务id获取区域列表

### 参数

| 名称         | 类型    | 说明     |
| ------------ | -------| -------- |
| `taskId` | string |  任务Id |

### 返回值 `Promise.<Boolean>`




### 请求示例

```javascript
...
try {
  const res =await this.axRobot.cancelTaskV3(this.taskId)
  console.log('cancelTaskV3 Success:', res)
  // cancelTaskV3 Success: true
} catch (error) {
  console.log('cancelTaskV3 Error:', error)
}
...
```

### 响应数据示例

```JSON
...
true or false
...
```


