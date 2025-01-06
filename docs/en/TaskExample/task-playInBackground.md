# Play background music

Provide task examples for the following scenarios:

Playing background music in the task is mainly achieved by setting local audio actions in the current point data

```typescript
  const task1 = {
    ...
    "curPt": { // current point info (unnecessary)
      ...
	  stepActs: [
		{
			type: 5, 
			data: {
				"audioId": "...", // audioId
				"interval": -1, // required
				"mode": 2, // mode
				"playInBackground": true // Whether to play background music true: background music must be played
			}
		}
	  ]
    },
    ...
  }
  const success = axRobot.startTask(task1)

```
