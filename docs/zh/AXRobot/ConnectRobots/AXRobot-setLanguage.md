# 设置语言

## `setLanguage(languge) -> {Promise.<boolean>}`

设置语言

### 参数

| 名称       | 类型   | 说明                                                       |
| ---------- | ------ | ---------------------------------------------------------- |
| `language` | number | 语言标识<br />1 - 简体中文<br />2 - 英文<br />3 - 繁体中文<br />4 - 日语<br />5 - 韩语 |

### 返回值 `Promise.<boolean>`

是否成功

* `true` - 成功
* `false` - 失败

### 示例

```typescript
...
succcess := await axRobot.setLanguage(1);
if (success) {
  ...
} else {
  ...
}
...
```

