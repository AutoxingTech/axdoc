# Get task template

Due to feedback from many friends that it is difficult to encapsulate tasks on their own, JS SDK has encapsulated a template for creating task request parameters. Users only need to input where and what to do, and the SDK will automatically encapsulate the request parameters. Users only need to call the startTask method.


Create complex point tasks:：

```typescript
  
// 获get robot all poi list
const result = await axRobot.getPoiList({
    robotId: "<robotId>"
});
const poiList = result.list

//get complex task template
// add a poi to taskNodeList
let poiInfo = poiList[0] 
// action --- What do you want to do
poiInfo.stepActs = [
    {
        type: 18,   // wait
        data: {
            pauseTime: 5
        }
    }
]
const taskNodeList = [poiInfo] // poiList
const addTaskParams = {
    name: 'task ' + new Date().getTime(), // task name
    runNum: 1 // runNum
}
// addTaskParams is not necessary. Default: name: 'task ' + new Date().getTime(),  runNum: 1 
const taskComplexTemplate = await axRobot.getTaskComplexTemplate(taskNodeList, addTaskParams)
const addTaskRes = await axRobot.startTask(taskComplexTemplate)
if (addTaskRes) {
    console.log("Complex task add success")
}

```
Create area tasks:

```typescript
  
// get all area list
const result = await getShelvesAreaList({robotId: 'robotId', isRelatedShelves: true, isAll: true})
const shelvesAreaList = console.log(result.list); // shelves areas 
const areaInfo = shelvesAreaList[0]
areaInfo.stepActs = [
    {
        type: 47,
        "data": {
            "useAreaId": areaInfo.id // shelves area id
        }
    }
]
const areaNodeList = [areaInfo]
// get  area task template
const taskAreaTemplate = await axRobot.getTaskAreaTemplate(areaNodeList, addTaskParams)
const addTaskAreaRes = await axRobot.startTask(taskAreaTemplate)
if (addTaskRes) {
     console.log("Area task add success")
}


```
