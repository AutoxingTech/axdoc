# PlayAudio

Play Audio

## Enum

| Name       | Data Type | Description                                                             |
| ---------- | --------- |-------------------------------------------------------------------------|
| `mode`     | number    | 1: Host computer processing, 2: Chassis processing                      |
| `url`      | string    | audio address                                                           |
| `audioId`  | string    | local audio resource ID <br/>'3111012': // Task started <br/>'3111002': // Arrived at destination <br/>'3111007': // Continue task <br/>'3111011': // Obstacle encountered <br/>'3111025': // Birthday wishes <br/>'3111026': // Start leading <br/>'3111027': // Lead to destination <br/>'3111018': // Incorrect item reminder <br/>'3111001': // Forceful pushing reminder <br/>'3111003': // Charging station not found <br/>'3111005': // Passed through turnstile <br/>'3111008': // Passed through automatic door <br/>'3111016': // Elevator arrived <br/>'3111006': // Entering elevator <br/>'3111014': // Failed to enter elevator <br/>'3111010': // Button pressed inside elevator <br/>'3111009': // Floor reached <br/>'3111017': // Help call inside elevator <br/>'3112044': // Lifting <br/>'3112045': // Lifting completed <br/>'3112046': // Unloading <br/>'3112047': // Task completed <br/>'3112048': // Invalid shelf detection point <br/>'3112049': // Shelf not detected <br/>'3112050': // Exceeded retry limit for docking <br/>'3112051': // Shelf position occupied <br/>'3112052': // Unable to reach unloading point                                                |
| `volume`   | number    | volume, value 0-100                                                     |
| `interval` | number    | Circular broadcast interval, unit: second, -1 means broadcast only once |
| `num`      | number    | Total Plays                                                             |
| `duration` | number    | Total playing time, unit: second                                        |



### notes
*   eg: If you want to play audio in other languages, you need to replace the second digit "1" with the corresponding country code, such as changing English 31xx012 to 32xx012
*   Currently, the supported country codes are: 1 Chinese 2 English, 3 Traditional, 4 Japanese, 5 Korean, 6 German, 7 Thailand, 8 Spain, 9 Poland, 10 Russian, 11 French, 12 Vietnam, 13 Czech, 14 Italy, 15 Türkiye
*   The fourth bit of audioId 1:Normal mode  2:Factory mode   eg Restaurant Voice: 31x1012   Factory voice: 31x2012 



