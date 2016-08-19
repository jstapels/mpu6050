# MPU6050

Minimal Node.js module for reading the raw data from an MPU6050.

This module has been tested on a BeagleBone Black.

## Install

```
npm install mpu6050
```

## API Reference

* MPU6050(device, address)
* initialize()
* testConnection(callback(err, data))
* getDeviceID(callback(err, data))
* setDeviceID(id)
* getFullScaleGyroRange(callback(err, data))
* setFullScaleGyroRange(range)
* getFullScaleAccelRange(callback(err, data))
* setFullScaleRange(range)
* getAcceleration(callback(err, data))
* getMotion6(callback(err, data))
* getRotation(callback(err, data))
* getSleepEnabled(callback(err, data))
* setSleepEnabled(enabled)
* getClockSource(callback(err, data))
* setClockSource(source)


## Usage

```javascript
var mpu6050 = require('mpu6050');

// Instantiate and initialize.
var mpu = new mpu6050();
mpu.initialize();

// Test the connection before using.
mpu.testConnection(function(err, testPassed) {
  if (testPassed) {
    mpu.getMotion6(function(err, data){
      console.log(data);
    });
    // Put the MPU6050 back to sleep.
    mpu.setSleepEnabled(1);
  }
});

```

