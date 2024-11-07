# set Weight Speed Limit

## `setWeightSpeedLimit(args) -> {Promise.<boolean>}`

Rotational angular velocity limit
### Parameters

| Name | Data Type | Description |
|--------|-----------|-----|
| `args` | {type: 0} |  0: disable; 1: enable  |

### Return value `Promise.<boolean>`

whether succeed

* `true` - success
* `false` - fail

### Example

```typescript
...
axRobot.setWeightSpeedLimit({type: 1}); //Enable rotational angular velocity speed limit
...
```

