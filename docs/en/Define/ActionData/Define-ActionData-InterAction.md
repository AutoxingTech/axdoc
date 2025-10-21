# ActionData - InterAction

Waiting for interactive action parameters

## Attributes

| Name | Data Type | Description |
| ----------- | -------- | ---------------------------------- |
| `pauseTime` | number   | Pause time, unit: seconds<br/>0 indicates no waiting |

## Example

```typescript
{
  "type": ActionType.InterAction,
  "data": {
    "pauseTime": 20
  }
}
```

