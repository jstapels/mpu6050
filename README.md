MPU6050
=======

Minimal Node.js module for reading the raw data from an MPU6050.

Usage
=====

```javascript
> var mpu6050 = require('mpu6050')
undefined
> var mpu = new mpu6050()
undefined
> mpu.initialize() # initialize the module
undefined
> mpu.testConnection() # always good to test the I2C connection first
true
> mpu.getMotion6() # get the raw data
[ 16,
  356,
  15828,
  -47,
  66,
  40 ]
> mpu.getMotion6()
[ -56,
  424,
  15848,
  -20,
  48,
  51 ]
> mpu.setSleepEnabled(1) # put back to sleep when finished
undefined
```

