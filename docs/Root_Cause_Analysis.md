# Root Cause Analysis

## QA-01: LDR Does Not Detect Darkness Correctly

### Problem
The automatic street light does not respond correctly when the environment becomes dark.

### 5-Why Analysis

Why 1: The LED does not turn ON correctly because the Arduino is not detecting the expected low-light condition.

Why 2: The expected low-light condition is not detected because the sensor reading does not match the selected threshold.

Why 3: The sensor reading does not match the threshold because the threshold was not sufficiently calibrated.

Why 4: The threshold was not sufficiently calibrated because different lighting conditions were not included in the initial testing.

Why 5: Different lighting conditions were not included because a systematic sensor calibration procedure was not defined.

### Root Cause
Insufficient LDR calibration and testing under different lighting conditions.

### Corrective Action
Test the LDR under different lighting conditions and adjust the threshold based on observed readings.


## QA-02: LED Remains ON in Bright Light

### Problem
The LED remains ON when sufficient light is detected.

### Root Cause
Incorrect threshold condition or unsuitable threshold value.

### Corrective Action
Verify the sensor readings and correct the threshold comparison logic.


## QA-03: Unsuitable Switching Threshold

### Problem
The LED changes state at an unsuitable light level.

### Root Cause
The threshold value was not properly calibrated using observed sensor readings.

### Corrective Action
Test different light conditions and adjust the threshold based on the observed readings.


## QA-04: QA Documentation Problem

### Problem
Test results are not systematically documented.

### Root Cause
A standard QA documentation format was not defined.

### Corrective Action
Create a structured QA test report containing test ID, expected result, actual result and status.
