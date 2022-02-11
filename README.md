# WLED_Firmware_Files

Create builds:

- Bot auf dem WLED Discord:
  - ./build custom
  - [env:esp32dev_mod]
board = esp32dev
platform = ${esp32.platform}
build_unflags = ${common.build_unflags}
build_flags = ${common.build_flags_esp32} -D WLED_RELEASE_NAME=ESP32 -D USERMOD_SSDR -D USERMOD_SN_PHOTORESISTOR #-D WLED_DISABLE_BROWNOUT_DET
lib_deps = ${esp32.lib_deps}
monitor_filters = esp32_exception_decoder
board_build.partitions = ${esp32.default_partitions}


## Lazy_Grid_Clock:

[env:esp32dev_mod]  
board = esp32dev  
platform = ${esp32.platform}  
build_unflags = ${common.build_unflags}  
build_flags = ${common.build_flags_esp32} -D WLED_RELEASE_NAME=ESP32 -D USERMOD_SSDR -D USERMOD_SN_PHOTORESISTOR #-D WLED_DISABLE_BROWNOUT_DET  
lib_deps = ${esp32.lib_deps}  
monitor_filters = esp32_exception_decoder  
board_build.partitions = ${esp32.default_partitions}  

[env:nodemcuv2_mod]  
board = nodemcuv2  
platform = ${common.platform_wled_default}  
platform_packages = ${common.platform_packages}  
board_build.ldscript = ${common.ldscript_4m1m}  
build_unflags = ${common.build_unflags}  
build_flags = ${common.build_flags_esp8266} -D WLED_RELEASE_NAME=ESP8266 -D WLED_DISABLE_ALEXA -D USERMOD_SSDR -D USERMOD_SN_PHOTORESISTOR  
lib_deps = ${esp8266.lib_deps}  

H: 0,22,21;0,1,2;2,3,4;4,17,26;24,25,26;22,23,24;2,19,24:44,65,66;44,45,46;46,47,48;48,61,70;68,69,70;66,67,68;46,63,68  
M: 6,15,28;6,7,8;8,9,10;10,11,32;30,31,32;28,29,30;8,13,30:50,59,72;50,51,52;52,53,54;54,55,76;74,75,76;72,73,74;52,57,74
