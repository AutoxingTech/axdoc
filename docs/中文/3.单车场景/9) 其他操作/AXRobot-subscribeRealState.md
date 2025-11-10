# 订阅机器人状态

## `subscribeRealState(listener) -> {void}`

订阅机器人实时状态

### 参数

| 名称       | 数据类型                                   | 说明                   |
| ---------- | ------------------------------------------ | ---------------------- |
| `listener` | [OnRobotListner](../../8.数据定义/Define-OnRobotListener) | 机器人实时状态订阅回调 |

### 返回值

无

### 示例

```typescript
...
axRobot.subscribeRealState({
  onStateChanged: state => {
    console.log(state.isManualMode); // 是否推动模式
    console.log(state.isTasking); // 是否正在执行任务
    console.log(state.isCharging); // 是否正在充电
    console.log(state.isRemoteMode); // 是否远程控制
    console.log(state.battery); // 当前电量（百分比）
    console.log(state.robotId); // 机器人标识
    console.log(state.speed); // 当前速度（m/s）
    console.log(state.areaId); // 当前区域ID
    console.log(state.isEmergencyStop); // 是否急停状态
    console.log(state.x); // 位置坐标的 x 分量
    console.log(state.y); // 位置坐标的 y 分量
    console.log(state.yaw); // 当前角度（弧度）
    console.log(state.locQuality); // 当前定位质量（0-100）
    console.log(state.hasObstruction); // 当前是否存在障碍物
    console.log(state.errors); // 故障码
    console.log(state.isGoHome); // 是否正在回桩充电中
    console.log(state.timestamp); // 机器人状态的时间戳
    // do something
  }
});
...
```

