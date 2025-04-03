# 三色灯控制

## 方法

## `setSerialPortLight(cmds) → {Promise.<any>}`

打开三色灯

### 参数

| 名称   | 类型      | 说明 |
| ------ |---------|--|
| `cmds` | Objecct | 指令集合:{"cmds": ["A0 01 01 A2"]} <br/>关闭黄灯：A0 01 00 A1 <br/>打开黄灯：A0 01 01 A2 <br/>黄灯闪烁：A0 01 02 A3 <br/>关闭绿灯：A0 02 00 A2 <br/>打开绿灯：A0 02 01 A3 <br/>绿灯闪烁：A0 02 02 A4 <br/>关闭红灯：A0 03 00 A3 <br/>打开红灯：A0 03 01 A4<br/> 红灯闪烁：A0 03 02 A5 <br/>关闭蜂鸣：A0 04 00 A4 <br/>打开蜂鸣：A0 04 01 A5 <br/>间断蜂鸣：A0 04 02 A6 <br/>关闭红灯+蜂鸣：A0 07 00 A7 <br/>打开红灯+蜂鸣：A0 07 01 A8 <br/>红灯闪烁+蜂鸣：A0 07 02 A9 <br/>关闭全部：A0 00 00 A0 <br/>打开全部：A0 00 01 A1 <br/>全部闪烁：A0 00 02 A2 <br/>备注：SDK 1.0.119以上支持此功能|

### 返回值 `Promise.<any>`

指令结果

* `{`
*  `"code": 0,` // 0: 成功；1：设备不存在；2：串口打开失败；3：指令发送失败
*   `"data": [{ `// 指令发送和反馈信息
*   `"feedback": "A00101A2",`
*   `"cmd": "A00101A2"`
*   `}],`
*   `"errText": "error"` // 错误信息
*   `}`

### 示例

```javascript
...
const success = await axRobot.setSerialPortLight("<cmds>");
...
```

