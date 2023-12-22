# axRobot 初始化失败

axRobot 初始化失败


## 返回值
???+ failure "axRobot 初始化失败"
=== "javascript"
    ```javascript
    { 
        errCode: 33000, 
        errText: 'Initialization failed. Please check app id and app secret.', 
        robotId: undefined 
    }
    ```
=== "json"

    ```json
    { 
        errCode: 33000, 
        errText: 'Initialization failed. Please check app id and app secret.', 
        robotId: undefined 
    }
    ```

## 处理方法
- 请检查app id和app secret 是否正确。
- 请检查 axRobot 构造函数参数中，serverUrl和websocketUrl是否正确。