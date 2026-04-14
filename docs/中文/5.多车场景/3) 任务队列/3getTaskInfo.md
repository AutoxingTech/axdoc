# 获取任务详情

## 方法(版本： 1.0.138及以上)

## `getQueueTaskDetails(taskId, needDetail) -> {Promise.<any>}`

根据业务id获取区域列表

### 参数

| 名称         | 类型    | 说明     |
| ------------ | -------| -------- |
| `taskId` | string |  任务Id |
| `needDetail` | boolean |  是否需要详细信息，默认false <BR/>false或不传：返回简略信息<BR/>true：返回详细信息（包含任务点、动作等）<BR/>版本： 1.0.139及以上|

### 返回值 `Promise.<any>`

任务详情

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `taskId` | string |  任务标识 |
| `taskType` | integer |  任务类型<BR/>0 消杀<BR/>1 回充电桩<BR/>2 餐厅<BR/>3 酒店<BR/>4 送物(五合一)<BR/>5 工厂<BR/>6 底盘小程序<BR/>7 充电调度 |
| `creatorName` | string |  任务创建者名称 |
| `taskStatus` | integer |  任务状态码<BR/>-1 未知状态<BR/>0 待分配（队列任务专用）<BR/>1 已分配待执行<BR/>2 执行中<BR/>3 暂停中<BR/>4 已完成<BR/>5 已取消（待执行时取消）<BR/>6 已取消（执行时取消）<BR/>7 已取消（待分配时取消，队列任务专用）<BR/>8 失败 |
| `taskStatusName` | string |  任务状态名称（中文）<BR/>未知<BR/>待分配<BR/>已分配待执行<BR/>执行中<BR/>暂停中<BR/>已完成<BR/>已取消(待执行时取消)<BR/>已取消(执行时取消)<BR/>已取消(待分配时取消)<BR/>失败 |
| `taskStatusNameEN` | string |  任务状态名称（英文）<BR/>unknown<BR/>waiting_assign<BR/>pending<BR/>running<BR/>paused<BR/>completed<BR/>cancelled_before_exec<BR/>cancelled_during_exec<BR/>cancelled_waiting<BR/>failed |
| `businessId` | string |  所属业务标识 |
| `robotId` | string |  执行任务的机器人标识 |
| `createTime` | integer |  任务创建时间，单位：毫秒 |
| `updateTime` | integer |  任务更新时间，单位：毫秒 |
| `issueTime` | integer |  任务下发时间，单位：毫秒 |
| `startTime` | integer |  任务开始执行时间，单位：毫秒 |
| `endTime` | integer |  任务结束时间，单位：毫秒 |
| `endType` | string |  任务结束类型<BR/>success 成功完成<BR/>cancel 取消<BR/>error 异常结束 |
| `dispatchType` | integer |  调度类型<BR/>0 无调度（普通任务）<BR/>1 RCS调度<BR/>2 队列任务 |
| `sourceType` | integer |  任务来源类型<BR/>0 未知来源<BR/>1 头壳APP<BR/>2 底盘小程序<BR/>3 呼叫器<BR/>4 底盘<BR/>5 调度<BR/>6 二次开发<BR/>7 平板APP |

<!-- 未执行任务：

| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `name` | string |  任务名称(required) |
| `businessId` | string |  业务标识，如果创建队列任务，则该字段必传；如果是普通任务，则该字段可以为空 |
| `robotId` | string |  执行任务的机器人标识，如果创建普通任务，则该字段必传；如果是队列任务，则该字段可以为空，但要保证 businessId 对应的业务下有机器人 |
| `dispatchType` | integer |  任务类型 0 普通任务  2 队列任务 |
| `runNum` | integer |  执行次数 默认为1,0表示无限循环 |
| `taskType` | integer |  任务类型 0 消杀 1 回充电桩 2 餐厅 3 酒店 4 送物(五合一) 5 工厂 6 底盘小程序 7 充电调度 |
| `runType` | integer |   运行类型 0 定时消杀 1 临时消杀 20 快捷送餐 21 多点送餐 22 直达 23 巡游 24 返航 25 充电桩26 召唤 27 生日模式 28 引领 29 顶升 30 顶升巡游31 灵活搬运32 辊筒33 满电离桩 |
| `routeMode` | integer |  行驶模式,默认为1 1 灵活躲避障碍 2 按轨迹行驶小范围避障 3 按轨迹行驶不避障 4 按轨迹行驶不补货架对接点 5分段算路 |
| `ignorePublicSite` | boolean | 是否忽略公共站点,默认是不忽略 |
| `speed` | integer |   机器人行驶速度，单位：米/秒 建议速度 0.4~1.0 |
| `sourceType` | integer |  任务来源类型 二开要求必须是6 |
| `curPt` | object |  机器人当前位置  |
| `taskPts` | array |  任务点列表 |
| `backPt` | object |  返航点 |


执行任务：


| 名称         | 类型           | 说明            |
| ------------ | ------------- | --------------  |
| `taskInfo` | [TaskInfo](../../8.数据定义/Define-TaskInfo.md) | 任务信息 | -->



### 请求示例

```javascript
...
try {
  const res = await this.axRobot.getQueueTaskDetails(this.taskId)
  console.log('getQueueTaskDetails Success:', res)
} catch (error) {
  console.log('getQueueTaskDetails Error:', error)
}
...
```




