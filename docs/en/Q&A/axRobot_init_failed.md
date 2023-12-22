# axRobot Initialization Failed

axRobot initialization failed.

## Return Value

???+ failure "axRobot initialization failed"
    ```javascript
    { 
        errCode: 33000, 
        errText: 'Initialization failed. Please check app id and app secret.', 
        robotId: undefined 
    }
    ```

## Troubleshooting
- Please check if the app id and app secret are correct.
- Please check if the `serverUrl` and `websocketUrl` in the axRobot constructor parameters are correct.