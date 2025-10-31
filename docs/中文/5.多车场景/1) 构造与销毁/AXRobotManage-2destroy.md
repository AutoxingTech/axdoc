# 释放


???+ example 

    === "无需等待销毁结果"
        ## `destroy() -> {void}`

        销毁机器人操作实例

        ### 参数

        无

        ### 返回值

        无

        ### 示例

        ```typescript
        ...
        axRobot.destroy();
        ...
        ```
    === "需要等待销毁结果"
        ## `destroyConnect() -> {Promise.<boolean>}`

        销毁机器人操作实例

        ### 参数

        无

        ### 返回值

        是否成功

        * `true` - 成功
        * `false` - 失败

        ### 示例

        ```typescript
        ...
        const success  = await axRobot.destroyConnect();
        if (success) {
            // 销毁成功后继续操作
        }
        ...
        ```

