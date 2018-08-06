This is the list of the code I contributed during GSoC 2018.

[ArduPilot main repo](https://github.com/ArduPilot/ardupilot):
==============================================================

 - Added gps and mag UAVCAN support to SITL
     - https://github.com/ArduPilot/ardupilot/pull/8509
     - Ready to be merged
     - List of commits:
        1. [Tools: Added new board type sitlcan, --uavcan argument to sim_vehicle.py and script to set up vcan0 interface](https://github.com/ArduPilot/ardupilot/pull/8509/commits/f851a6830f448e59474cfc0b9255e449f04fedbf)
        2. [AP_Arming: Updated pre-arm checks to not test calibration when we are feeding data we know is correct](https://github.com/ArduPilot/ardupilot/pull/8509/commits/0381e5baa13a9c37a2b39ba9558da00f0daf8d46)
        3. [SITL: Added GPS_TYPE_CAN](https://github.com/ArduPilot/ardupilot/pull/8509/commits/a2f0fdeb2fbb298929b930904bf816408db8be18)
        4. [AP_UAVCAN: Updated registration of compass sensor node and changed spin to spinOnce in AP_UAVCAN.cpp because spin was never exiting on Ubuntu](https://github.com/ArduPilot/ardupilot/pull/8509/commits/0037bd59de75b3debbfb2f31a2bc4cfb06fd953a)
        5. [AP_HAL_SITL: added gps and mag UAVCAN support to SITL. Added UAVCAN arguments to SITL launch args. sitl_gps.cpp now sends data over CAN when CAN is enabled.](https://github.com/ArduPilot/ardupilot/pull/8509/commits/0919c21b13f1b5ba0761a7a09d098d2969ad650d)
        6. [AP_HAL: Added proper defines for when using CAN in SITL](https://github.com/ArduPilot/ardupilot/pull/8509/commits/c73bd913d1ce5e905a95d7dc8943e68edd18d7c4)
        7. [AP_Compass: Added proper includes, CAN backend logic and proper data interpretation](https://github.com/ArduPilot/ardupilot/pull/8509/commits/56b7c9559643d8dcced771c986c181504a269dbb)
        8. [AP_BoardConfig: Added CANManager and appropriate headers for SITL](https://github.com/ArduPilot/ardupilot/pull/8509/commits/fd216b4d7f547c8ad77b94f6318b7d5704bc0728)

[OpenMotorDrive framework fork](https://github.com/d-v/framework):
==================================================================

- [Updated bootloader Makefile to allow debugging through gdb](https://github.com/d-v/framework/commit/57842c113edcfc2e7f55b12ca909b1b8cfdb9b03)
- [Updated Makefile to use appropriate modules and be possible to debug through gdb](https://github.com/d-v/framework/commit/3b218a79edf5c62cfe4d3e1caecd7e01e8a7c493)
- [Updated openocd.cfg to work with my specific type of generic JST debugger](https://github.com/d-v/framework/commit/c352395ca3c57df1360b9a506180c04b6ff4c4fd)
- [Set proper PAL line mode for Pixracers USART port](https://github.com/d-v/framework/commit/6a236f8d21e91b66ed9ac607fb8f3ce51c08a4db)
- [Created appropriate board.h file for Pixracer](https://github.com/d-v/framework/commit/f1ce9b9378115eaeff117e61014cfeec98e3e80b)
- [Created appropriate makefile for Pixracer](https://github.com/d-v/framework/commit/962c9045efb0f9586c703b5404a880e826336dfb)
- [Created mcuconf.h file appropriate to Pixracer](https://github.com/d-v/framework/commit/3ebe6b599f2f25d14d062f2798dd8f93d4a91698)
- [Added boot delay for convenience and made sure that USART2 is being used](https://github.com/d-v/framework/commit/895091fd82852c62516dd230db2dc81e78238df1)
- [Enabled param module](https://github.com/d-v/framework/commit/006990c54db713c67609fd10020e02ffa4b194f0)
- [Made sure serial is being used, the buffer is the right size, that mutexes are enabled and usart waits](https://github.com/d-v/framework/commit/3605b693e0af319880fee5ff6f9688ec8241b047)
- [Added high priority worker thread for interrupt exceptions](https://github.com/d-v/framework/commit/032047b9e5134501b7fdd73d7c015ac44bd76b67)
- [Added code for USART-UAVCAN bridge](https://github.com/d-v/framework/commit/28e5f0df0c5df3a53e2d4988e04ce1ba573c2fe4)
- [Added Python test script](https://github.com/d-v/framework/commit/d7d83bb52ea6c2b925af7ac3737068cf49bbfb5e)
- [Updated ChibiOS to support interrupt exceptions](https://github.com/d-v/framework/commit/797d3e16e3ec7d2d03a83c91556ded4276bbf677)
- [Updated dsdl that supports Tom's tunnel messages](https://github.com/d-v/framework/commit/c108472de834e82d5e9f229de7d8414c1920ba03)

[ArduPilot wiki](https://github.com/ArduPilot/ardupilot_wiki):
==============================================================

- Added instructions to enable Mavlink over UAVCAN
    - https://github.com/ArduPilot/ardupilot_wiki/pull/1360
    - Ready to be merged
    - List of commits:
        1. [Added instructions to enable Mavlink over UAVCAN](https://github.com/ArduPilot/ardupilot_wiki/pull/1360/commits/45dc598b38c58f8296bc65e2bdf0536f8b79952a)
- Added information on GDB debugging through JTAG
    - https://github.com/ArduPilot/ardupilot_wiki/pull/1361
    - Ready to be merged
    - List of commits:
        1. [added instructions for st-link debugging on pixracer](https://github.com/ArduPilot/ardupilot_wiki/pull/1361/commits/8e70b3f44ea088bc82377b12d1e1bd22add9ed1f)
        2. [Updated to specify required version of OpenOCD and added information about the other version of ST-Link debugger that exists](https://github.com/ArduPilot/ardupilot_wiki/pull/1361/commits/2415d2aba3ccf061a8840dc7b290352634d73e1e)

Progress updates posted on ArduPilot Discourse:
===============================================

- [GSoC 2018: UAVCAN over SITL](https://discuss.ardupilot.org/t/gsoc-2018-uavcan-over-sitl/29887)
- [GSoC 2018: USART UAVCAN Bridge (wip)](https://discuss.ardupilot.org/t/gsoc-2018-usart-uavcan-bridge-wip/30519)
- [USART-Tunnel Bridge Firmware](https://discuss.ardupilot.org/t/usart-tunnel-bridge-firmware/30718)
- [GSoC 2018: USART-UAVCAN bridge completed](https://discuss.ardupilot.org/t/gsoc-2018-usart-uavcan-bridge-completed/31449)