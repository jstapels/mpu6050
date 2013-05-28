# MPU6050

Minimal Node.js module for reading the raw data from an MPU6050.

This module has been tested on a BeagleBone Black.

## Install

```
npm install mpu6050
```

## Usage

```javascript
var mpu6050 = require('mpu6050')
var mpu = new mpu6050()
mpu.initialize()

if (mpu.testConnection()) {
  console.log(mpu.getMotion6());
}
mpu.setSleepEnabled(1)
```

