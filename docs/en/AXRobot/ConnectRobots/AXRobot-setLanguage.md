# Set Language

## `setLanguage(languge) -> {Promise.<boolean>}`

Set language

### Parameters

| Name       | Type   | Description                                                  |
| ---------- | ------ | ------------------------------------------------------------ |
| `language` | number | Language Code<br />1 - Chinese Simplified<br />2 - English<br />3 - Chinese Traditional <br />4 - Japanese<br />5 - Korean |

### Return Value `Promise.<boolean>`

Whether the execution is successful

* `true` - success
* `false` - fail

### Example

```javascript
...
succcess := await axRobot.setLanguage(1);
if (success) {
  ...
} else {
  ...
}
...
```

