## Telemetry Data

Data were sent from the Donkey Gym server as JSON objects with the data in the table below. Each JSON was written as a row in a CSV file named `data.csv`, as was the current lap (which I had to track separately).

Images strings were decoded and saved in an `images` directory.

Both `data.csv` and `images` were saved to a trial directory named with the time in `hh-mm-ss` format, and each of those directories was saved in a directory named with the date in `dd-mm-yy` format.

This structure made it easy to keep track of first the manual recordings, then the trial recordings.

|Columns|Type||Description|
|:---|:---:|:---|:---|
|**steering_angle**|continuous||direction of front wheels versus direction of travel, -0.64 (left) to 0.64 (right)|
|**throttle**|continuous||throttle input, -1.0 (brake) to 1.0 (forward throttle) |
|**speed**|continuous||speed in meters per second|
|**image**|string||image from simulated camera as a base-64 encoded string|
|**hit**|nominal||object with which the car is in contact at the recorded instant|
|**time**|string||time since start of simulation in seconds|
|**accel_x**|continuous||acceleration in the *camera* x axis in meters per seconds squared|
|**accel_y**|continuous||acceleration in the *camera* y axis in meters per seconds squared|
|**accel_z**|continuous||acceleration in the *camera* z axis in meters per seconds squared|
|**gyro_x**|continuous||rotation around *camera* x axis in radians per second|
|**gyro_y**|continuous||rotation around *camera* y axis in radians per second|
|**gyro_z**|continuous||rotation around *camera* z axis in radians per second|
|**gyro_w**|continuous||rotation around *camera* w axis in radians per second|
|**pitch**|continuous||angle of lengthwise (front to back) tilt in degrees from horizontal|
|**yaw**|continuous||compass heading in degrees|
|**roll**|continuous||angle of widthwise (left to right) tilt in degrees from horizontal|
|**cte**|continuous||distance from designated center line, which is often--but not necessarily--the middle of the track|
|**activeNode**|ordinal||number of current track segment|
|**totalNodes**|discrete||total number of track segments, 307 for mini-monaco track|
|**pos_x**|continuous||position in meters from arbitrary origin on *camera* x axis|
|**pos_y**|continuous||position in meters from arbitrary origin on *camera* y axis|
|**pos_z**|continuous||position in meters from arbitrary origin on *camera* z axis|
|**vel_x**|continuous||instantaneous velocity in meters per second on *camera* x axis|
|**vel_y**|continuous||instantaneous velocity in meters per second on *camera* y axis|
|**vel_z**|continuous||instantaneous velocity in meters per second on *camera* z axis|
|**on_road**|boolean||whether car is currently on track (not implemented for mini-monaco track)|
|**progress_on_shortest_path**|continuous||distance in meters along specified shortest path (not implemented for mini-monaco track)|
|**lap**\*|ordinal||number of "collisions" with starting line, used primarily for timing|

<font size="1">note: Lap data was not included in the telemetry message from the server. Current lap was tracked separately, then added before writing to CSV.</font>