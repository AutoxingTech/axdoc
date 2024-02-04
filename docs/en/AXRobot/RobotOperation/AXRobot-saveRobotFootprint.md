# saveRobotFootprint

## `saveRobotFootprint(footprintInfo) -> {Promise.<boolean>}`

Set robot contour lines



### Parameters

| Name  | Data Type | Description                    |
| ---------- |--------|------------------|
| `footprintInfo`     | any |  Robot contour line collection |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example
!!! note "Example"
    ```javascript
    ...
    const success = await axRobot.saveRobotFootprint({footprint: [[0.248, 0.108], [0.24, 0.174], [0.231, 0.207], [0.211, 0.236], ...]});
    console.log(success); // Is the robot contour line set successfully
    ...
    ```



