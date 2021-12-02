## Telemetry Data

Telemetry data were sent from the Donkey Gym server as JSON objects. The fields of each telemetry message JSON were written as one row in a CSV file named `data.csv`, as was the current lap (which I had to track separately).

Image strings were decoded and saved in an `images` directory.

Both `data.csv` and `images` were saved to a directory named with the `hh-mm-ss` trial start time, and each directory was saved in the relevant `dd-mm-yyyy` date directory.

This structure made it easy to keep track of first the manual recordings, then the trial recordings.

Ultimately, only the `11-12-2012/19-28-18` data set was used.