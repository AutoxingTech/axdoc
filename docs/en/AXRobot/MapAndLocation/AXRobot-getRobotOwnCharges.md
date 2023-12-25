# Get Bound Charging Pile

## `getRobotOwnCharges() -> {Promise.<any>}`

Get the list of charging piles bound to the robot

### Parameters

none

### Return value `Promise.<any>`

Charging pile list

### Example

```javascript
...
const charges = await axRobot.getRobotOwnCharges();

console.log(charges.count); // number of charging piles
console.log(charges.list); // charging pile list
charges.list.forEach(chargingPile => {
   console.log(chargingPile.areaId); // The identification of the area where the charging pile is located
   console.log(chargingPile.buildingId); // ID of the building where the charging pile is located
   console.log(chargingPile.businessId); // ID of the business to which the charging pile belongs
   console.log(chargingPile.floor); // The floor where the charging pile is located
   console.log(chargingPile.id); // Charging Pile ID
   console.log(chargingPile.name); // charging pile name
   console.log(chargingPile.coordinate); // The coordinates of the charging pile, the format is [x, y]; such as [13.411045089526397,-6.95027412476179]
   console.log(chargingPile.yaw); // The angle value of charging pile facing Unit: degree
});
...
```
