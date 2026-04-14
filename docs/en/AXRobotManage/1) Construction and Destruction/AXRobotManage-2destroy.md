````markdown
# Destroy


???+ example 

    === "No need to wait for destruction result"
        ## `destroy() -> {void}`

        Destroy robot operation instance

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
    === "Need to wait for destruction result"
        ## `destroyConnect() -> {Promise.<boolean>}`

        Destroy robot operation instance

        ### Parameters

        None

        ### Return Value

        Whether successful

        * `true` - Success
        * `false` - Failure

        ### Example

        ```typescript
        ...
        const success  = await axRobot.destroyConnect();
        if (success) {
            // Continue operation after successful destruction
        }
        ...
        ```


````
