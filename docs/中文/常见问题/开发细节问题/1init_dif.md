# AXRobot与AXRobotManage

## 1. AXRobot 与 AXRobotManage 区别

> * **1:** 通道接口用处不同  
    AXRobot 主要是单车通道的接口，AXRobotManage 主要是业务通道的接口；  
    但是AXRobotManage 继承了 AXRobot，所以 AXRobotManage 也可以调用 AXRobot 的接口。
> * **2:** 初始化构造函数不同  
  AXRobot: 五个参数
    ```typescript
    const axRobot = new AXRobot("<appId>", "<appSecret>", Mode, "<serverUrl>", "<websocketUrl>");
    ```
  AXRobotManage: 一个参数对象
    ```typescript
    const axRobot = AXRobotManage({
      appId: "",
      secret: "",
      mode: "",
      serverUrl: '',
      wsUrl: '',
      viewLanguage： ''
    })
    ```

> * **3:** AXRobotManage要求版本在1.0.123及以上
