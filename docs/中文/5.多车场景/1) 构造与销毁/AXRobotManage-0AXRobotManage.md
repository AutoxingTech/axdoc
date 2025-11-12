# 继承之前AXRobot
AXRobotManage继承之前AXRobot，之前AXRobot方法在AXRobotManage实例化后同样适用。

#  业务通道(多车) 与 单车通道
业务通道和单车通道是不同的两个通道，互相之前没有影响；  
如果单车通道想连其他的车，必须先销毁之前的单车连接；  
业务要切换业务也是必须先销毁之前的业务连接。

#  开发思路引导
订阅业务：监听多车实时状态，一般可以用于多车状态监测；但是如果想对车控制或者发起指令、任务等，还是需要连接单车通道

#  AXRobotManage 构造函数

## `AXRobotManage({appId: "", secret: "", mode:  "mode", serverUrl: '', wsUrl: ''， viewLanguage： ''})`

构造函数

### 参数

| 名称     | 数据类型 | 说明     |
| -------- | -------- | -------- |
| `appId` | string   | 应用 ID，可向相关运营人员申请提供 |
| `appSecret` | string   | 数据请求密钥，可向相关运营人员申请提供 |
| [`AppMode`](../../8.数据定义/Define-AppMode.md) | string   | 应用模式 |
| `serverUrl` | string   |可选 <br> 如果不填，服务默认使用国服接入点<br> serverUrl: <br>国服接入点:"https://api.autoxing.com/"<br>海外接入点:"https://apiglobal.autoxing.com/"<br> |
| `websocketUrl` | string   | 可选 <br> 如果不填，服务默认使用国服接入点<br>websocketUrl:<br>国服接入点:"wss://service.autoxing.com/"<br>海外接入点:"wss://serviceglobal.autoxing.com/" |
| `viewLanguage` | `viewLanguage` | string   | 异常返回的默认语言（目前支持中英文，默认英文 -- zh开头：中文 其它：英文）|



### 返回值

无

### 示例

???+ example 

    === "国服接入点"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 初始化
            const axRobot = new AXRobotManage({
                appId:appId, // 机器人管理平台根据权限获取appid
                secret: appSecret, // 机器人管理平台根据权限获取appSecret
                mode: AppMode.WAN_APP, // 应用模式:AppMode已在包内export，可直接引入
                serverUrl: serverUrl, // 私有化serverUrl 
                wsUrl: wsUrl, // 私有化wsUrl
                viewLanguage: getApp().globalData.language, // 语言 可不传
              }
            );
           

        ```

    === "海外接入"

        ```typescript
            import { AXRobotManage, AppMode } from "@autoxing/robot-js-sdk";

            // 创建 AXRobotManage 私有化实例
            const axRobot = new AXRobotManage(
              new AXRobot({
                appId:appId, // 机器人管理平台根据权限获取appid
                secret: appSecret, // 机器人管理平台根据权限获取appSecret
                mode: AppMode.WAN_APP, // 应用模式:AppMode已在包内export，可直接引入
                serverUrl: serverUrl, // serverUrl 
                wsUrl: wsUrl, // wsUrl
                viewLanguage: getApp().globalData.language, // 语言 可不传
              })
            );

        ```