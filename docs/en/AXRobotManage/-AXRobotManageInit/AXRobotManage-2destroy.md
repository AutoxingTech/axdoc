# Destroy


???+ example 

    === "No need to wait for results"
        ## `destroy() -> {void}`

        Example of robot destruction operation

        ### Parameters

        None

        ### Return Value

        None

        ### Example

        ```typescript
        ...
        axRobot.destroy();
        ...
        ```
    === "Need to wait for the results"
        ## `destroyConnect() -> {Promise.<boolean>}`

        Example of robot destruction operation

        ### Parameters

        None

        ### Return Value

        success

        * `true` - success
        * `false` - failed

        ### Example

        ```typescript
        ...
        const success  = await axRobot.destroyConnect();
        if (success) {
            // Continue operation after successful destruction
        }
        ...
        ```

