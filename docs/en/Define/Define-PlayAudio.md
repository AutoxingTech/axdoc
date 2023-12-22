# PlayAudio

Play Audio

## Enum

| Name       | Data Type | Description                                                             |
| ---------- | --------- | ----------------------------------------------------------------------- |
| `mode`     | number    | 1: Host computer processing, 2: Chassis processing                      |
| `url`      | string    | audio address                                                           |
| `audioId`  | string    | local audio resource ID                                                 |
| `volume`   | number    | volume, value 0-100                                                     |
| `interval` | number    | Circular broadcast interval, unit: second, -1 means broadcast only once |
| `num`      | number    | Total Plays                                                             |
| `duration` | number    | Total playing time, unit: second                                        |
