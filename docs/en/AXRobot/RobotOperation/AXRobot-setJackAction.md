# Set JackAction

## `setJackAction(type) -> {Promise.<boolean>}`

Set the lifting and lowering actions of the robot

### Parameters

| Name  | Data Type | Description                    |
| ---------- |--------|--------------------------------|
| `type`     | number | type: <br>  0 up <br>  1  down |

### Return value `Promise.<boolean>`

whether succeed

- true - success
- false - fail

### Example
!!! note "Example"
    ```javascript
    ...
    const success = await axRobot.setJackAction(0);
    ...
    ```
