Version 0.7.6 (2020-06-05)
========================
* 白熊猫即将被废弃，请升级为 comma 2 或者 黑熊猫
* 支持日产奇骏 2017, 聆风 2018-19 和 Rogue 2019（感谢 avolmensky）
* 支持马自达 CX-5 2017（仅录像模式，感谢 Jafaral）
* 通过使用 thneed 在模型中节约了大量 CPU 计算
* 大量的代码精简重构

Version 0.7.5 (2020-05-13)
========================
 * 支持右舵车型的驾驶员监控
 * 更新驾驶模型: 改进急转弯路况驾驶和前车速度检测
 * 更新驾驶员监控模型：Comma 2 上的整体改进
 * 在设置中新增前置摄像头预览开关，方便调整设备安装位置
 * 新增一些现代、起亚、Genesis 车型支持（感谢 xx979xx）
 * 支持日产奇骏 2019、日产聆风 2018（感谢 avolmensky）
 * 改进丰田 Rav4 2020 车型的横向控制

Version 0.7.4 (2020-03-20)
========================
 * 更新驾驶模型: 改进切换车道和前车检测
 * 更新驾驶员监控模型: 改进眨眼检测
 * 提高车辆校准稳定性
 * 改进丰田普锐斯 2019、2020 车型上的横向控制
 * 改进大众高尔夫车型上的横向控制：增加 20％ 转向扭矩
 * 修复丰田 CHR 2017、2018 车型上误用转向角传感器的问题
 * 支持本田 Insight （感谢 theantihero）
 * 精简代码（车辆抽象 和 UI 部分）

Version 0.7.3 (2020-02-21)
========================
 * 支持丰田汉兰达 2020（感谢 che220）
 * 支持雷克萨斯 NX 300h 2018 （感谢 kengggg）
 * 提升 ECU 固件查询速度
 * 修复停车熄火后，设备进程管理会挂掉的问题
 * 检测不到人脸时忽略驾驶员监控，支持直接遮挡摄像头
 * 可配置的 EON 基础屏幕亮度，在此基础上支持光感

Version 0.7.2 (2020-02-07)
========================
 * 基于ECU固件版本的指纹识别（丰田、本田车型）
 * 更新驾驶模型: 改善弯道和车道变换期间的路径预测并更好地追踪前车车速
 * 改善极端光线条件下的驾驶员监控，添加无法准确监控的警告
 * 支持丰田 Rav4 2019 混动（感谢 illumiN8i）
 * 支持雷克萨斯 RX 2016, 2017, 2020（感谢 illumiN8i）
 * 支持克莱斯勒 Pacifica 2020 混动（感谢 adhintz）

Version 0.7.1 (2020-01-20)
========================
 * comma two support!
 * Lane Change Assist above 45 mph!
 * Replace zmq with custom messaging library, msgq!
 * Supercombo model: calibration and driving models are combined for better lead estimate
 * More robust updater thanks to jyoung8607! Requires NEOS update
 * Improve low speed ACC tuning

Version 0.7 (2019-12-13)
========================
 * Move to SCons build system!
 * Add Lane Departure Warning (LDW) for all supported vehicles!
 * NEOS update: increase wifi speed thanks to jyoung8607!
 * Adaptive driver monitoring based on scene
 * New driving model trained end-to-end: improve lane lines and lead detection
 * Smarter torque limit alerts for all cars
 * Improve GM longitudinal control: proper computations for 15Hz radar
 * Move GM port, Toyota with DSU removed, comma pedal in community features; toggle switch required
 * Remove upload over cellular toggle: only upload qlog and qcamera files if not on wifi
 * Refactor Panda code towards ISO26262 and SIL2 compliancy
 * Forward stock FCW for Honda Nidec
 * Volkswagen port now standard: comma Harness intercepts stock camera

Version 0.6.6.2 (2019-11-12)
========================
 * Add fingerprint (2019 Chinese Levin Hybrid)
 * Make DBC preprocessing deterministic
 * Make visiond compile on pc

Version 0.6.6.1 (2019-11-08)
========================
 * Fix fan control when not plugged into panda
 * Fix unicode bug in DoUninstall reading

Version 0.6.6 (2019-11-05)
========================
 * Volkswagen support thanks to jyoung8607!
 * Toyota Corolla Hybrid with TSS 2.0 support thanks to u8511049!
 * Lexus ES with TSS 2.0 support thanks to energee!
 * Fix GM ignition detection and lock safety mode not required anymore
 * Log panda firmware and dongle ID thanks to martinl!
 * New driving model: improve path prediction and lead detection
 * New driver monitoring model, 4x smaller and running on DSP
 * Display an alert and don't start openpilot if panda has wrong firmware
 * Fix bug preventing EON from terminating processes after a drive
 * Remove support for Toyota giraffe without the 120Ohm resistor

Version 0.6.5.1 (2019-10-26)
========================
 * 优化中文翻译

Version 0.6.5 (2019-10-07)
========================
 * NEOS update: upgrade to Python3 and new installer!
 * comma Harness support!
 * New driving model: improve path prediction
 * New driver monitoring model: more accurate face and eye detection
 * Redesign offroad screen to display updates and alerts
 * Increase maximum allowed acceleration
 * Prevent car 12V battery drain by cutting off EON charge after 3 days of no drive
 * Lexus CT Hybrid support thanks to thomaspich!
 * Louder chime for critical alerts
 * Add toggle to switch to dashcam mode
 * Fix "invalid vehicle params" error on DSU-less Toyota

Version 0.6.4 (2019-09-08)
========================
 * Forward stock AEB for Honda Nidec
 * Improve lane centering on banked roads
 * Always-on forward collision warning
 * Always-on driver monitoring, except for right hand drive countries
 * Driver monitoring learns the user's normal driving position
 * Honda Fit support thanks to energee!
 * Lexus IS support

Version 0.6.3 (2019-08-12)
========================
 * Alert sounds from EON: requires NEOS update
 * Improve driver monitoring: eye tracking and improved awareness logic
 * Improve path prediction with new driving model
 * Improve lane positioning with wide lanes and exits
 * Improve lateral control on RAV4
 * Slow down for turns using model
 * Open sourced regression test to verify outputs against reference logs
 * Open sourced regression test to sanity check all car models

Version 0.6.2 (2019-07-29)
========================
 * New driving model!
 * Improve lane tracking with double lines
 * Strongly improve stationary vehicle detection
 * Strongly reduce cases of braking due to false leads
 * Better lead tracking around turns
 * Improve cut-in prediction by using neural network
 * Improve lateral control on Toyota Camry and C-HR thanks to zorrobyte!
 * Fix unintended openpilot disengagements on Jeep thanks to adhintz!
 * Fix delayed transition to offroad when car is turned off

Version 0.6.1 (2019-07-21)
========================
 * Remote SSH with comma prime and [ssh.comma.ai](https://ssh.comma.ai)
 * Panda code Misra-c2012 compliance, tested against cppcheck coverage
 * Lockout openpilot after 3 terminal alerts for driver distracted or unresponsive
 * Toyota Sienna support thanks to wocsor!

Version 0.6 (2019-07-01)
========================
 * New model, with double the pixels and ten times the temporal context!
 * Car should not take exits when in the right lane
 * openpilot uses only ~65% of the CPU (down from 75%)
 * Routes visible in connect/explorer after only 0.2% is uploaded (qlogs)
 * loggerd and sensord are open source, every line of openpilot is now open
 * Panda safety code is MISRA compliant and ships with a signed version on release2
 * New NEOS is 500MB smaller and has a reproducible usr/pipenv
 * Lexus ES Hybrid support thanks to wocsor!
 * Improve tuning for supported Toyota with TSS 2.0
 * Various other stability improvements

Version 0.5.13 (2019-05-31)
==========================
 * Reduce panda power consumption by 70%, down to 80mW, when car is off (not for GM)
 * Reduce EON power consumption by 40%, down to 1100mW, when car is off
 * Reduce CPU utilization by 20% and improve stability
 * Temporarily remove mapd functionalities to improve stability
 * Add openpilot record-only mode for unsupported cars
 * Synchronize controlsd to boardd to reduce latency
 * Remove panda support for Subaru giraffe

Version 0.5.12 (2019-05-16)
==========================
 * Improve lateral control for the Prius and Prius Prime
 * Compress logs before writing to disk
 * Remove old driving data when storage reaches 90% full
 * Fix small offset in following distance
 * Various small CPU optimizations
 * Improve offroad power consumption: require NEOS Update
 * Add default speed limits for Estonia thanks to martinl!
 * Subaru Crosstrek support thanks to martinl!
 * Toyota Avalon support thanks to njbrown09!
 * Toyota Rav4 with TSS 2.0 support thanks to wocsor!
 * Toyota Corolla with TSS 2.0 support thanks to wocsor!

Version 0.5.11 (2019-04-17)
========================
 * Add support for Subaru
 * Reduce panda power consumption by 60% when car is off
 * Fix controlsd lag every 6 minutes. This would sometimes cause disengagements
 * Fix bug in controls with new angle-offset learner in MPC
 * Reduce cpu consumption of ubloxd by rewriting it in C++
 * Improve driver monitoring model and face detection
 * Improve performance of visiond and ui
 * Honda Passport 2019 support
 * Lexus RX Hybrid 2019 support thanks to schomems!
 * Improve road selection heuristic in mapd
 * Add Lane Departure Warning to dashboard for Toyota thanks to arne182

Version 0.5.10 (2019-03-19)
========================
 * Self-tuning vehicle parameters: steering offset, tire stiffness and steering ratio
 * Improve longitudinal control at low speed when lead vehicle harshly decelerates
 * Fix panda bug going unexpectedly in DCP mode when EON is connected
 * Reduce white panda power consumption by 500mW when EON is disconnected by turning off WIFI
 * New Driver Monitoring Model
 * Support QR codes for login using comma connect
 * Refactor comma pedal FW and use CRC-8 checksum algorithm for safety. Reflashing pedal is required.
   Please see `#hw-pedal` on [discord](discord.comma.ai) for assistance updating comma pedal.
 * Additional speed limit rules for Germany thanks to arne182
 * Allow negative speed limit offsets

Version 0.5.9 (2019-02-10)
========================
 * Improve calibration using a dedicated neural network
 * Abstract planner in its own process to remove lags in controls process
 * Improve speed limits with country/region defaults by road type
 * Reduce mapd data usage with gzip thanks to eFiniLan
 * Zip log files in the background to reduce disk usage
 * Kia Optima support thanks to emmertex!
 * Buick Regal 2018 support thanks to HOYS!
 * Comma pedal support for Toyota thanks to wocsor! Note: tuning needed and not maintained by comma
 * Chrysler Pacifica and Jeep Grand Cherokee support thanks to adhintz!

Version 0.5.8 (2019-01-17)
========================
 * Open sourced visiond
 * Auto-slowdown for upcoming turns
 * Chrysler/Jeep/Fiat support thanks to adhintz!
 * Honda Civic 2019 support thanks to csouers!
 * Improve use of car display in Toyota thanks to arne182!
 * No data upload when connected to Android or iOS hotspots and "Enable Upload Over Cellular" setting is off
 * EON stops charging when 12V battery drops below 11.8V

Version 0.5.7 (2018-12-06)
========================
 * Speed limit from OpenStreetMap added to UI
 * Highlight speed limit when speed exceeds road speed limit plus a delta
 * Option to limit openpilot max speed to road speed limit plus a delta
 * Cadillac ATS support thanks to vntarasov!
 * GMC Acadia support thanks to CryptoKylan!
 * Decrease GPU power consumption
 * NEOSv8 autoupdate

Version 0.5.6 (2018-11-16)
========================
 * Refresh settings layout and add feature descriptions
 * In Honda, keep stock camera on for logging and extra stock features; new openpilot giraffe setting is 0111!
 * In Toyota, option to keep stock camera on for logging and extra stock features (e.g. AHB); 120Ohm resistor required on giraffe.
 * Improve camera calibration stability
 * More tuning to Honda positive accelerations
 * Reduce brake pump use on Hondas
 * Chevrolet Malibu support thanks to tylergets!
 * Holden Astra support thanks to AlexHill!

Version 0.5.5 (2018-10-20)
========================
 * Increase allowed Honda positive accelerations
 * Fix sporadic unexpected braking when passing semi-trucks in Toyota
 * Fix gear reading bug in Hyundai Elantra thanks to emmertex!

Version 0.5.4 (2018-09-25)
========================
 * New Driving Model
 * New Driver Monitoring Model
 * Improve longitudinal mpc in mid-low speed braking
 * Honda Accord hybrid support thanks to energee!
 * Ship mpc binaries and sensibly reduce build time
 * Calibration more stable
 * More Hyundai and Kia cars supported thanks to emmertex!
 * Various GM Volt improvements thanks to vntarasov!

Version 0.5.3 (2018-09-03)
========================
 * Hyundai Santa Fe support!
 * Honda Pilot 2019 support thanks to energee!
 * Toyota Highlander support thanks to daehahn!
 * Improve steering tuning for Honda Odyssey

Version 0.5.2 (2018-08-16)
========================
 * New calibration: more accurate, a lot faster, open source!
 * Enable orbd
 * Add little endian support to CAN packer
 * Fix fingerprint for Honda Accord 1.5T
 * Improve driver monitoring model

Version 0.5.1 (2018-08-01)
========================
 * Fix radar error on Civic sedan 2018
 * Improve thermal management logic
 * Alpha Toyota C-HR and Camry support!
 * Auto-switch Driver Monitoring to 3 min counter when inaccurate

Version 0.5 (2018-07-11)
========================
 * Driver Monitoring (beta) option in settings!
 * Make visiond, loggerd and UI use less resources
 * 60 FPS UI
 * Better car parameters for most cars
 * New sidebar with stats
 * Remove Waze and Spotify to free up system resources
 * Remove rear view mirror option
 * Calibration 3x faster

Version 0.4.7.2 (2018-06-25)
==========================
 * Fix loggerd lag issue
 * No longer prompt for updates
 * Mitigate right lane hugging for properly mounted EON (procedure on wiki)

Version 0.4.7.1 (2018-06-18)
==========================
 * Fix Acura ILX steer faults
 * Fix bug in mock car

Version 0.4.7 (2018-06-15)
==========================
 * New model!
 * GM Volt (and CT6 lateral) support!
 * Honda Bosch lateral support!
 * Improve actuator modeling to reduce lateral wobble
 * Minor refactor of car abstraction layer
 * Hack around orbd startup issue

Version 0.4.6 (2018-05-18)
==========================
 * NEOSv6 required! Will autoupdate
 * Stability improvements
 * Fix all memory leaks
 * Update C++ compiler to clang6
 * Improve front camera exposure

Version 0.4.5 (2018-04-27)
==========================
 * Release notes added to the update popup
 * Improve auto shut-off logic to disallow empty battery
 * Added onboarding instructions
 * Include orbd, the first piece of new calibration algorithm
 * Show remaining upload data instead of file numbers
 * Fix UI bugs
 * Fix memory leaks

Version 0.4.4 (2018-04-13)
==========================
 * EON are flipped! Flip your EON's mount!
 * Alpha Honda Ridgeline support thanks to energee!
 * Support optional front camera recording
 * Upload over cellular toggle now applies to all files, not just video
 * Increase acceleration when closing lead gap
 * User now prompted for future updates
 * NEO no longer supported :(

Version 0.4.3.2 (2018-03-29)
============================
 * Improve autofocus
 * Improve driving when only one lane line is detected
 * Added fingerprint for Toyota Corolla LE
 * Fixed Toyota Corolla steer error
 * Full-screen driving UI
 * Improved path drawing

Version 0.4.3.1 (2018-03-19)
============================
 * Improve autofocus
 * Add check for MPC solution error
 * Make first distracted warning visual only

Version 0.4.3 (2018-03-13)
==========================
 * Add HDR and autofocus
 * Update UI aesthetic
 * Grey panda works in Waze
 * Add alpha support for 2017 Honda Pilot
 * Slight increase in acceleration response from stop
 * Switch CAN sending to use CANPacker
 * Fix pulsing acceleration regression on Honda
 * Fix openpilot bugs when stock system is in use
 * Change starting logic for chffrplus to use battery voltage

Version 0.4.2 (2018-02-05)
==========================
 * Add alpha support for 2017 Lexus RX Hybrid
 * Add alpha support for 2018 ACURA RDX
 * Updated fingerprint to include Toyota Rav4 SE and Prius Prime
 * Bugfixes for Acura ILX and Honda Odyssey

Version 0.4.1 (2018-01-30)
==========================
 * Add alpha support for 2017 Toyota Corolla
 * Add alpha support for 2018 Honda Odyssey with Honda Sensing
 * Add alpha support for Grey Panda
 * Refactored car abstraction layer to make car ports easier
 * Increased steering torque limit on Honda CR-V by 30%

Version 0.4.0.2 (2018-01-18)
==========================
 * Add focus adjustment slider
 * Minor bugfixes

Version 0.4.0.1 (2017-12-21)
==========================
 * New UI to match chffrplus
 * Improved lateral control tuning to fix oscillations on Civic
 * Add alpha support for 2017 Toyota Rav4 Hybrid
 * Reduced CPU usage
 * Removed unnecessary utilization of fan at max speed
 * Minor bug fixes

Version 0.3.9 (2017-11-21)
==========================
 * Add alpha support for 2017 Toyota Prius
 * Improved longitudinal control using model predictive control
 * Enable Forward Collision Warning
 * Acura ILX now maintains openpilot engaged at standstill when brakes are applied

Version 0.3.8.2 (2017-10-30)
==========================
 * Add alpha support for 2017 Toyota RAV4
 * Smoother lateral control
 * Stay silent if stock system is connected through giraffe
 * Minor bug fixes

Version 0.3.7 (2017-09-30)
==========================
 * Improved lateral control using model predictive control
 * Improved lane centering
 * Improved GPS
 * Reduced tendency of path deviation near right side exits
 * Enable engagement while the accelerator pedal is pressed
 * Enable engagement while the brake pedal is pressed, when stationary and with lead vehicle within 5m
 * Disable engagement when park brake or brake hold are active
 * Fixed sporadic longitudinal pulsing in Civic
 * Cleanups to vehicle interface

Version 0.3.6.1 (2017-08-15)
============================
 * Mitigate low speed steering oscillations on some vehicles
 * Include board steering check for CR-V

Version 0.3.6 (2017-08-08)
==========================
 * Fix alpha CR-V support
 * Improved GPS
 * Fix display of target speed not always matching HUD
 * Increased acceleration after stop
 * Mitigated some vehicles driving too close to the right line

Version 0.3.5 (2017-07-30)
==========================
 * Fix bug where new devices would not begin calibration
 * Minor robustness improvements

Version 0.3.4 (2017-07-28)
==========================
 * Improved model trained on more data
 * Much improved controls tuning
 * Performance improvements
 * Bugfixes and improvements to calibration
 * Driving log can play back video
 * Acura only: system now stays engaged below 25mph as long as brakes are applied

Version 0.3.3  (2017-06-28)
===========================
  * Improved model trained on more data
  * Alpha CR-V support thanks to energee and johnnwvs!
  * Using the opendbc project for DBC files
  * Minor performance improvements
  * UI update thanks to pjlao307
  * Power off button
  * 6% more torque on the Civic

Version 0.3.2  (2017-05-22)
===========================
  * Minor stability bugfixes
  * Added metrics and rear view mirror disable to settings
  * Update model with more crowdsourced data

Version 0.3.1  (2017-05-17)
===========================
  * visiond stability bugfix
  * Add logging for angle and flashing

Version 0.3.0  (2017-05-12)
===========================
  * Add CarParams struct to improve the abstraction layer
  * Refactor visiond IPC to support multiple clients
  * Add raw GPS and beginning support for navigation
  * Improve model in visiond using crowdsourced data
  * Add improved system logging to diagnose instability
  * Rewrite baseui in React Native
  * Moved calibration to the cloud

Version 0.2.9  (2017-03-01)
===========================
  * Retain compatibility with NEOS v1

Version 0.2.8  (2017-02-27)
===========================
  * Fix bug where frames were being dropped in minute 71

Version 0.2.7  (2017-02-08)
===========================
  * Better performance and pictures at night
  * Fix ptr alignment issue in boardd
  * Fix brake error light, fix crash if too cold

Version 0.2.6  (2017-01-31)
===========================
  * Fix bug in visiond model execution

Version 0.2.5  (2017-01-30)
===========================
  * Fix race condition in manager

Version 0.2.4  (2017-01-27)
===========================
  * OnePlus 3T support
  * Enable installation as NEOS app
  * Various minor bugfixes

Version 0.2.3  (2017-01-11)
===========================
  * Reduce space usage by 80%
  * Add better logging
  * Add Travis CI

Version 0.2.2  (2017-01-10)
===========================
  * Board triggers started signal on CAN messages
  * Improved autoexposure
  * Handle out of space, improve upload status

Version 0.2.1  (2016-12-14)
===========================
  * Performance improvements, removal of more numpy
  * Fix boardd process priority
  * Make counter timer reset on use of steering wheel

Version 0.2  (2016-12-12)
=========================
  * Car/Radar abstraction layers have shipped, see cereal/car.capnp
  * controlsd has been refactored
  * Shipped plant model and testing maneuvers
  * visiond exits more gracefully now
  * Hardware encoder in visiond should always init
  * ui now turns off the screen after 30 seconds
  * Switch to openpilot release branch for future releases
  * Added preliminary Docker container to run tests on PC

Version 0.1  (2016-11-29)
=========================
  * Initial release of openpilot
  * Adaptive cruise control is working
  * Lane keep assist is working
  * Support for Acura ILX 2016 with AcuraWatch Plus
  * Support for Honda Civic 2016 Touring Edition
