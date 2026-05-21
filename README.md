# MPU-9250 STM32 Library with DMP

STM32 HAL C port of the SparkFun MPU-9250 Arduino library, with DMP (Digital Motion Processor) support. Built and tested on STM32F103C8 (Blue Pill).

## Why this exists

The MPU-9250 is a 9-axis IMU (accelerometer, gyroscope, magnetometer) with an onboard DMP that produces quaternion output without spending host MCU cycles. SparkFun supports the part on Arduino, but loading the DMP firmware blob and bringing it up on STM32 with the HAL stack requires undocumented register-level work. This port does that.

## Features

- DMP firmware loading and configuration on STM32 HAL
- Quaternion output from the DMP
- Raw accel, gyro, mag readings with configurable full-scale ranges
- FIFO-based DMP data readout
- Complete STM32CubeIDE project: `.ioc`, linker script, and HAL configuration included

## Hardware

- MCU: STM32F103C8 (Blue Pill). Portable to any STM32 with the same HAL peripherals.
- Sensor: TDK InvenSense MPU-9250 IMU.

## Note

The MPU-9250 is end-of-life as of 2018. For new designs, use the ICM-20948 port: [`ICM20948_STM32Library`](https://github.com/A-R-Hariri/ICM20948_STM32Library).

## Credits

Original library: SparkFun MPU-9250 Arduino Library (MIT).

## Author

Amir Hariri.
