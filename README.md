
# Acknowledgement
All work completed by BF developers past present and future is fully acknowledged and supported. This repository of binaries is hosted until such time that Betaflight (hopefully) supports it directly.

Source code here:
https://github.com/ShikOfTheRa/betaflight/tree/Sentinel-antenna-tracker-support
Purchasers of Sentinel product may request source code directly for a specific version if required. 


# Betaflight versions precompiled for Sentinel

A pull request for the Sentinal AAT will shortly submitted into betaflight.
Until that version is release, the Betaflight FC's can be flashed manually using the following process  


## Betaflight flash process (when using same version as existing board)
* Backup / dump CLI contents of your existing board into a file
* Determine which board / betaflight target you use. e.g Matek F411
* Open the config file for your board from here. e.g. MTKS-MATEKF411:
  * https://github.com/betaflight/unified-targets/tree/master/configs/default
* Identify the unified target from within the config file
  * It will be the second word in the file e.g. MAtek F411 unified target is STMF411 (# Betaflight / STM32F411in file)  
* Flash the unified target
* Connect with Betaflight GUI configurator
* Enter CLI and copy / paste the backup
* Save / reboot
* Your FC is now updated and ready 


## Betaflight flash process (when using a different version to existing board)
* Determine which board / betaflight target you use. e.g Matek F411
* Open the config file for your board from here. e.g. MTKS-MATEKF411:
  * https://github.com/betaflight/unified-targets/tree/master/configs/default
* Identify the unified target from within the config file
  * It will be the second word in the file e.g. MAtek F411 unified target is STMF411 (# Betaflight / STM32F411in file)  
* Flash the unified target
* Connect with Betaflight GUI configurator
* Enter CLI and copy /paste the contents of your target config file into the cli
* Save / reboot
* Your FC is now updated and ready 

## Betaflight manual target flash process
* Install fonts from the x.xx\fonts folder to your flight controller using the Betaflight GUI (OSD tab>Font Manger>Open Font File>Open downloaded font>Upload Font

## Enabling AAT on the FC
* Enable AAT telemetry in the cli: set osd_telemetry = ON
* Power AAT/RX and FC and verify telemetry is received by LED or the web browser

