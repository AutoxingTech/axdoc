# Three-color Light Control

## Method

## `setSerialPortLight(cmds) → {Promise.<any>}`

Turn on the three-color light.

### Parameters

| Name   | Type      | Description |
| ------ |---------|--|
| `cmds` | Objecct | Command set: {"cmds": ["A0 01 01 A2"]} <br/>Turn off yellow light: A0 01 00 A1 <br/>Turn on yellow light: A0 01 01 A2 <br/>Yellow light blinking: A0 01 02 A3 <br/>Turn off green light: A0 02 00 A2 <br/>Turn on green light: A0 02 01 A3 <br/>Green light blinking: A0 02 02 A4 <br/>Turn off red light: A0 03 00 A3 <br/>Turn on red light: A0 03 01 A4 <br/>Red light blinking: A0 03 02 A5 <br/>Turn off buzzer: A0 04 00 A4 <br/>Turn on buzzer: A0 04 01 A5 <br/>Intermittent buzzer: A0 04 02 A6 <br/>Turn off red light + buzzer: A0 07 00 A7 <br/>Turn on red light + buzzer: A0 07 01 A8 <br/>Red light blinking + buzzer: A0 07 02 A9 <br/>Turn off all: A0 00 00 A0 <br/>Turn on all: A0 00 01 A1 <br/>All blinking: A0 00 02 A2 <br/>Note: Supported from SDK version 1.0.119 onwards|

### Return Value `Promise.<any>`

Command result

* `{`
*  `"code": 0,` // 0: Success; 1: Device not found; 2: Serial port open failed; 3: Command sending failed
*   `"data": [{ `// Command sending and feedback information
*   `"feedback": "A00101A2",`
*   `"cmd": "A00101A2"`
*   `}],`
*   `"errText": "error"` // Error message
*   `}`

### Example

```javascript
...
const success = await axRobot.setSerialPortLight("<cmds>");
...
```

