# 订阅任务状态

## 方法

## `subscribeTaskState(listener) -> {void}`

订阅任务状态。

### 参数

| 名称       | 类型                                      | 说明         |
| ---------- | ----------------------------------------- | ------------ |
| `listener` | [OnTaskListener](#/Define-OnTaskListener) | 任务状态回调 |

### 返回值 `void`

### 示例

```javascript
...
axRobot.subscribeTaskState({
  onTaskChanged: (state: any) => {
    console.log(state.actType); // 任务状态动作类型 1000-任务开始  14-出发  16-到达  40-等待交互  1001-任务完成
    console.log(state.data); // 具体任务状态数据
  }
});
...
```



