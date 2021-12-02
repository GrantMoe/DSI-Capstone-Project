## Data Dictionary 

The Donkey Gym server sends JSON telemetry messages every simulation frame. The default rate is 60 frames per second.

|Columns|Type|Description|
|:---|:---|:---|
|**steering_angle<sup>1</sup>**|continuous|ratio of current steering input to maximum steering input|
|**throttle<sup>2</sup>**|continuous|ratio of turtent throttle input to maximum throttle input|
|**speed**|continuous|speed (meters per second)|
|**image<sup>3</sup>**|string|camera output frame (base-64-encoded string)|
|**hit**|nominal|object with which the car is in contact|
|**time**|string|time since start of simulation (seconds)|
|**accel_x<sup>3</sup>**|continuous|acceleration in the *camera* x axis (meters per seconds squared)|
|**accel_y<sup>3</sup>**|continuous|acceleration in the *camera* y axis (meters per seconds squared)|
|**accel_z<sup>3</sup>**|continuous|acceleration in the *camera* z axis (meters per seconds squared)|
|**gyro_x<sup>3</sup>**|continuous|rotation around *camera* x axis (radians per second)|
|**gyro_y<sup>3</sup>**|continuous|rotation around *camera* y axis (radians per second)|
|**gyro_z<sup>3</sup>**|continuous|rotation around *camera* z axis (radians per second)|
|**gyro_w<sup>3</sup>**|continuous|rotation around *camera* w axis (radians per second)|
|**pitch**|continuous|angle of lengthwise (front to back) tilt from horizontal (degrees)|
|**yaw**|continuous|compass heading (degrees)|
|**roll**|continuous|angle of widthwise (left to right) tilt from horizontal (degrees)|
|**cte (cross track error)**|continuous|distance from track-dependent center line (meters)|
|**activeNode**|ordinal|numbered label of current track segment|
|**totalNodes<sup>4</sup>**|discrete|total number of track segments|
|**pos_x**|continuous|position from arbitrary origin on *camera* x axis (meters)|
|**pos_y**|continuous|position from arbitrary origin on *camera* y axis (meters)|
|**pos_z**|continuous|position from arbitrary origin on *camera* z axis (meters)|
|**vel_x**|continuous|instantaneous velocity on *camera* x axis (meters per second)|
|**vel_y**|continuous|instantaneous velocity on *camera* y axis (meters per second)|
|**vel_z**|continuous|instantaneous velocity on *camera* z axis (meters per second)|
|**on_road<sup>5</sup>**|boolean|whether car is currently on track|
|**progress_on_shortest_path<sup>5</sup>**|continuous|distance along specified shortest path (meters)|
|**lap<sup>6</sup>**|ordinal|number of "collisions" with starting line|

<font size="1">1. -0.64 (full left) to 0.64 (full right)</font>  
<font size="1">2. -1.0 (full brake) to 1.0 (full forward throttle)</font>  
<font size="1">3. simulated sensor output</font>  
<font size="1">4. mini-monaco: 307</font>  
<font size="1">5. mini-monaco: not implemented</font>  
<font size="1">6. not provided by server; added by client</font>  