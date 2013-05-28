MPU6050
=======

Minimal Node.js module for reading the raw data from an MPU6050.

Usage
=====

```javascript
> var mpu6050 = require('mpu6050')
> var mpu = new mpu6050()
> mpu.initialize()
> mpu.testConnection()
true
> mpu.getMotion6()
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
> mpu.setSleepEnabled(1)
```

