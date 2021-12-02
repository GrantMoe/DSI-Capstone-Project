## Data Dictionary 

The Donkey Gym server sends JSON telemetry messages every simulation frame. The default rate is 60 frames per second.

|Columns|Type|Description|
|:---|:---|:---|
|**steering_angle**|continuous|direction of front wheels versus direction of travel, -0.64 (left) to 0.64 (right)|
|**throttle**|continuous|throttle input, -1.0 (brake) to 1.0 (forward throttle) |
|**speed**|continuous|speed (meters per second)|
|**image**|string|simulated camera image encoded in base-64|
|**hit**|nominal|object with which the car is in contact at the recorded instant|
|**time**|string|time since start of simulation (seconds)|
|**accel_x**|continuous|acceleration in the *camera* x axis (meters per seconds squared)|
|**accel_y**|continuous|acceleration in the *camera* y axis (meters per seconds squared)|
|**accel_z**|continuous|acceleration in the *camera* z axis (meters per seconds squared(|
|**gyro_x**|continuous|rotation around *camera* x axis (radians per second)|
|**gyro_y**|continuous|rotation around *camera* y axis (radians per second)|
|**gyro_z**|continuous|rotation around *camera* z axis (radians per second)|
|**gyro_w**|continuous|rotation around *camera* w axis (radians per second)|
|**pitch**|continuous|angle of lengthwise (front to back) tilt from horizontal (degrees)|
|**yaw**|continuous|compass heading (degrees)|
|**roll**|continuous|angle of widthwise (left to right) tilt from horizontal (degrees)|
|**cte**|continuous|Cross Track Error - distance from designated center line, which is often--but not necessarily--the middle of the track (meters)|
|**activeNode**|ordinal|numbered label of current track segment|
|**totalNodes**|discrete|total number of track segments, 307 for mini-monaco track|
|**pos_x**|continuous|position from arbitrary origin on *camera* x axis (meters)|
|**pos_y**|continuous|position from arbitrary origin on *camera* y axis (meters)|
|**pos_z**|continuous|position from arbitrary origin on *camera* z axis (meters)|
|**vel_x**|continuous|instantaneous velocity on *camera* x axis (meters per second)|
|**vel_y**|continuous|instantaneous velocity on *camera* y axis (meters per second)|
|**vel_z**|continuous|instantaneous velocity on *camera* z axis (meters per second)|
|**on_road**|boolean|whether car is currently on track. not implemented for mini-monaco|
|**progress_on_shortest_path**|continuous|distance along specified shortest path (meters). not implemented for mini-monaco|
|**lap**|ordinal|number of "collisions" with starting line, used primarily for timing|

<font size="1">1. simulated sensor output</font>  
<font size="1">2. not provided by server; added by client</font>