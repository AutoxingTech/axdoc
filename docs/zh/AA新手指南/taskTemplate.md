# 获取创建任务请求参数模板

因很多朋友反馈在任务上自己封装较为困难，js-sdk封装了创建任务请求参数模板，用户只需要输入到哪，做什么，sdk会自动封装好请求参数，用户只需要调用 startTask 方法即可。


创建复杂点位任务：

```typescript
  
// 获取机器人所有点位数据
const result = await axRobot.getPoiList({
    robotId: "<robotId>"
});
const poiList = result.list

// 获取复杂任务请求参数模板
// 添加一个点位 // 到哪
let poiInfo = poiList[0] 
// 当前点位动作 --- 做什么
poiInfo.stepActs = [
    {
        type: 18,   //到达停留时间
        data: {
            pauseTime: 5
        }
    }
]
const taskNodeList = [poiInfo] // 点集合
const addTaskParams = {
    name: 'task ' + new Date().getTime(), // 任务名称
    runNum: 1 // 循环次数
}
// addTaskParams可不传 默认name: 'task ' + new Date().getTime(),  runNum: 1 
const taskComplexTemplate = await axRobot.getTaskComplexTemplate(taskNodeList, addTaskParams)
const addTaskRes = await axRobot.startTask(taskComplexTemplate)
if (addTaskRes) {
    console.log("复杂任务发起成功")
}

```
创建区对区任务：

```typescript
  
// 获取所有货架区
const result = await getShelvesAreaList({robotId: 'robotId', isRelatedShelves: true, isAll: true})
const shelvesAreaList = console.log(result.list); // 货架区列表 
const areaInfo = shelvesAreaList[0]
areaInfo.stepActs = [
    {
        type: 47,
        "data": {
            "useAreaId": areaInfo.id // 货架区 id
        }
    }
]
const areaNodeList = [areaInfo]
// 获取区对区任务请求参数模板
const taskAreaTemplate = await axRobot.getTaskAreaTemplate(areaNodeList, addTaskParams)
const addTaskAreaRes = await axRobot.startTask(taskAreaTemplate)
if (addTaskRes) {
    console.log("区队区任务发起成功")
}


```
