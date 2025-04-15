#  自动识别货架尺寸指令

操作流程 开始识别-> 推动机器人的同时获取货架尺寸信息 -> 结束识别（获取到机器人尺寸信息后） -> 保存识别到的货架信息


## 开始识别
### `detectRackSize({type: number}) -> {Promise.<boolean>}`

#### 参数

| 名称       | 类型     | 说明                  |
| ---------- |--------|---------------------|
| `type`     | number | 识别货架  0：开始识别；1：结束识别 |

#### 返回值 `Promise.<boolean>`

指令下发是否成功

- true - 成功
- false - 失败

#### 示例

```typescript
...
const success = await axRobot.setJackAction({type: 0});
...
```




## 获取货架尺寸信息
### `getRackSize() -> {Promise.<any>}`


#### 返回值 `Promise.<any>`

获取货架尺寸信息建议一秒钟查询一次


#### 示例

```typescript
...
const rackSizeInfo = await axRobot.setJackAction({type: 0});
// rackSizeInfo:  {"pose":{"pos":[-0.932,-1.379],"ori":-1.743},"width":0.65,"height":0.72}
...
```



## 设置货架尺寸信息
### `setRackSize(args) -> {Promise.<boolean>}`

#### 参数

| 名称     | 类型  | 说明                                                                |
|--------|-----|-------------------------------------------------------------------|
| `args` | any | 获取到的货架尺寸信息 eg: {"pose":{"pos":[-0.932,-1.379],"ori":-1.743},"width":0.65,"height":0.72} |


#### 返回值 `Promise.<boolean>`

是否成功

- true - 成功
- false - 失败


#### 示例

```typescript
...
const success = await axRobot.setRackSize(args);
...
```





