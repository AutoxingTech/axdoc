# 释放


???+ example 

    === "销毁实例"
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
    === "断连车"
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

