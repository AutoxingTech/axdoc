# Get Network Mode

## `getRouteMode() -> {Promise.<string>}`

Get Robot Network Mode

### Parameters

none

### Return value `Promise.<string>`

Network Mode

### Example

```javascript
const mode = await axRobot.getRouteMode();
console.log(mode); 
```

> * **explain:** Return value：etho_first: "Head shell WIFI network supply"/"Head shell 4G network supply"(you can judge by yourself according to whether the head shell is connected to wifi), wlan0_first: "Chassis WIFI network supply", usbo_first: "Chassis 4G network supply"

