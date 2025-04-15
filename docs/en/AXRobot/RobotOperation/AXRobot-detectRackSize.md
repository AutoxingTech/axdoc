#  Identify shelves

Operation process: Start recognition -> Drive the robot to obtain shelf size information -> End recognition (after obtaining the robot size information) ->Save the recognized shelf information


## 1.Enable it
### `detectRackSize({type: number}) -> {Promise.<boolean>}`

#### Parameters

| Name  | Data Type | Description                    |
| ---------- |--------|---------------------|
| `type`     | number | Identify shelves  0：Enable it；1：End recognition |

#### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

#### Example

```typescript
...
const success = await axRobot.setJackAction({type: 0});
...
```




## 2.Obtain shelf size information
### `getRackSize() -> {Promise.<any>}`


#### Return value `Promise.<any>`

Suggest querying shelf size information once a second


#### Example

```typescript
...
const rackSizeInfo = await axRobot.setJackAction({type: 0});
// rackSizeInfo:  {"pose":{"pos":[-0.932,-1.379],"ori":-1.743},"width":0.65,"height":0.72}
...
```



## 3.Set shelf size information
### `setRackSize(args) -> {Promise.<boolean>}`

#### Parameters

| Name  | Data Type | Description                                                                                            |
|--------|-----|--------------------------------------------------------------------------------------------------------|
| `args` | any | Obtained shelf size information eg: {"pose":{"pos":[-0.932,-1.379],"ori":-1.743},"width":0.65,"height":0.72} |


#### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

#### Example

```typescript
...
const success = await axRobot.setRackSize(args);
...
```





