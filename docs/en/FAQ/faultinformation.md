| Fault Code | Status                        | Troubleshooting Method                                           
|------------|-------------------------------|------------------------------------------------------------------
| 0002       | Failed to fetch map           | Restart the robot or restart the chassis service.                |
| 0003       | Starting point outside map    | Adjust the starting point position on the mapping platform to ensure it is within the map. |
| 0004       | Endpoint outside map          | Adjust the endpoint position on the mapping platform to ensure it is within the map. |
| 0005       | Starting point not in traversable area | Check if virtual walls are blocking the map information.          |
| 0006       | Endpoint not in traversable area | Check if virtual walls are blocking the map information.          |
| 0007       | Starting point and endpoint are the same | Redefine the starting and ending points.                         |
| 0009       | Path not connected            | Check if there are virtual walls obstructing the route.           |
| 0100       | Exceeded retry attempts for charging | Check for obstacles around the charging station and observe if the robot docks with it. |
| 0101       | Charging base not recognized  | Ensure the charging station is powered and the robot is correctly docked. |
| 0102       | Did not receive successful signal from charging station | Ensure the charging station is powered and unobstructed.         |
| 1000       | System error                  | Restart the service.      |     
| 1001                            | Request for control service abnormal    | Restart the service                                              |
| 1002                            | Route control failed                    | Restart the service                                              |
| 1003                            | Map server not running                  | Restart the service                                              |
| 1004                            | Mapping failed                         | Restart the robot                                                |
| 1005                            | During positioning or mapping, no obstacle avoidance map /maps/5cm message for more than 1s | Restart the robot                        |
| 1007                            | Wheel speed is 0 for more than 15 seconds alarm | 1. Obstacles block all passageways; 2. Robot positioning lost, push charging pile for charging pile reset |
| 1008                            | Robot moves for more than 1 minute without exceeding 1 meter range alarm | Same as 1007                                                     |
| 3001                            | Odom not running                        | Restart the robot                                                |
| 3002                            | Odom message frequency abnormal         | Restart the robot                                                |
| 4001                            | Imu not running                         | Restart the robot                                                |
| 4002                            | Imu message frequency abnormal          | Restart the robot                                                |
| 4003                            | Imu angular velocity abnormal           | Restart the robot                                                |
| 4004                            | Vertical angle abnormal                 | Restart the robot                                                |
| 5001                            | Lidar not running                       | Restart the robot                                                |
| 5002                            | Lidar message frequency abnormal        | Restart the robot                                                |
| 5003                            | Lidar scan time abnormal                | Restart the robot                                                |
| 6010                            | Abnormal shutdown reminder              | 1. Shutdown via blue button on client homepage; 2. Press chassis power button for 5s to shut down, directly turn off chassis main power or press power button for more than 10s will trigger this exception |
| 7001                            | Localization anomaly                    | 1. Click the manual reset button to manually drag the robot icon on the map to set the pose; 2. Push back to the charging pile for reset       |
| 7002                            | Inaccurate localization quality         | Same as 7001                                                     |
| 7003                            | Localization mapping message frequency abnormal | Same as 7001                                                   |
| 100001                          | No available floors                    | 1. Check if the business bound to the robot has a map; 2. Create a new map and update it to the chassis after marking                   |
| 100002                          | No station data                        | Same as 100001                                                   |
| 38001                           | Not deployed                          | Please bind this robot SN to the business                           |
| 38023                           | Cross-floor charging pile              | Select the charging pile of the current floor in the settings        |
| 38023                           | Cross-floor standby point              | Select the standby point of the current floor in the settings        |
| 34006                           | Websocket connection timeout           | The head and chassis are disconnected. If the error persists after restarting the entire machine, check if the Ethernet cable is loose between them |
| 35008                           | Invalid task ID                        | Often occurs when cloud tasks initiated from multiple ends (e.g., mini programs) are not synchronized to the chassis. Check if the vehicle's network is normal, ensure normal network operation, and recreate the cloud task |
| 38006                           | Failed to create task                  | Same as 35008                                                    |
| 38008                           | Failed to cancel task                  | Same as 35008                                                    |
| 38011                           | Failed to end task                     | Same as 35008                                                    |
| 38016                           | Failed to update task                  | Same as 35008                                                    |
| 38017                           | Failed to execute task                 | Same as 35008                                                    |
| 6010                            | Abnormal shutdown                     | 1. Client clicks "I know"                                        |
| 8007                            | Lost laser radar                      | 1. Client waits for countdown 60 seconds to recover automatically; 2. Restart the robot to attempt recovery              |
| 11007                           | Depth camera's power-off guard needs to be powered off for Juyou         | Same as 8007                                                     |
| 11012                           | Depth camera's power-off guard may need to be powered off for ihawk      | Same as 8007                                                     |
| 9016                            | Lifting device error                  
| 9017                            | Sensor fusion node /optical_flow_fusion_node not running              |
| 9018                            | Rack detection node /rack_detector_node not running                    |
| 9501                            | Debug node opened                                                    |
| 9502                            | ax-cache has .params.yaml, this configuration file is deprecated      |
| 9503                            | Detected optical flow hardware, but not configured to use              |
| 10001                           | Exceeded retry attempts on pile, no touch signal detected               |
| 10002                           | Charging dock not recognized                                         |
| 10003                           | Exceeded retry attempts on pile, no current received after touch        |
| 11001                           | camera_node Juyou node not running                                   |
| 11002                           | /depth_camera/forward message frequency abnormal (deprecated)          |
| 11003                           | /depth_camera/downward message frequency abnormal (deprecated)         |
| 11004                           | /depth_camera/forward reported error (deprecated)                     |
| 11005                           | /depth_camera/downward reported error (deprecated)                    |
| 11006                           | Depth camera hardware not found (deprecated)                          |
| 11007                           | Juyou depth camera reported error                                    |
| 11008                           | RGB camera hardware not found                                        |
| 11009                           | /rgb_camera_node node not running                                    |
| 11010                           | RGB camera other errors                                              |
| 11011                           | ihawk_node node not running                                          |
| 11012                           | ihawk depth camera reported error                                    |
| 9017                            | Sensor fusion node /optical_flow_fusion_node not running             |
| 9018                            | Rack detection node /rack_detector_node not running                   |
| 9501                            | Debug node opened                                                   |
| 9502                            | ax-cache has .params.yaml, this configuration file is deprecated     |
| 9503                            | Detected optical flow hardware, but not configured to use             |
| 10001                           | Exceeded retry attempts on pile, no touch signal detected             | 
| 10002                           | Charging dock not recognized                                        |
| 10003                           | Exceeded retry attempts on pile, no current received after touch      | 
| 11001                           | camera_node Juyou node not running                                  |
| 11002                           | /depth_camera/forward message frequency abnormal (deprecated)         |
| 11003                           | /depth_camera/downward message frequency abnormal (deprecated)        |
| 11004                           | /depth_camera/forward reported error (deprecated)                    |
| 11005                           | /depth_camera/downward reported error (deprecated)                   |
| 11006                           | Depth camera hardware not found (deprecated)                          |
| 11007                           | Juyou depth camera reported error                                    |
| 11008                           | RGB camera hardware not found                                        |
| 11009                           | /rgb_camera_node node not running                                    |
| 11010                           | RGB camera other errors                                              |
| 11011                           | ihawk_node node not running                                          |
| 11012                           | ihawk depth camera reported error                                    |
| 11013                           | ihawk depth camera depth value abnormal, possibly obscured (reserved) | 
| 11501                           | Depth camera not calibrated|
| 11013                           | ihawk depth camera depth value abnormal, possibly obscured (reserved) | 
| 11501                           | Depth camera not calibrated|

