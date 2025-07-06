# DRC200 by API
## Overview

Template for monitoring Digiton DRC200 device
Testing was performed on firmware 1.17 to 1.19. It is important to get and enter the variable {$DRC200TOKEN} into the macro for authorization and receiving data via API.
Template for 6 Zabbix. Macro {$STREAM.URL} and {$TUNER_FREQ} can also be configured separately for each device.

## Requirements

Zabbix server version 6.0 or higher.

### Tested version

Testing was performed on firmware 1.17 to 1.19


### Macros used

|Name|Description|Default|
|----|-----------|-------|
|{$CPU.UTIL.CRIT}|<p>Critical CLU load in %</p>|`90`|
|{$DRC200BITRATERECORDER}|<p>Setting the verifiable bitrate characteristics for the control recording</p>|`64000`|
|{{$DRC200RECCAPTUREPOINT}|<p>Setting the verifiable characteristics of the control entry pointss</p>|`output,tuner`|
|{{$DRC200RECUPLOADSTATUS}|<p>We set the verifiable characteristics of the control recording points and their upload to external storage</p>|`true,true`|
|{$DRC200TOKEN}|<p>A token for authorization on the device for polling it</p>|``|
|{$LOW.LEVEL}|<p>The value in LUFS that will be triggered for silence</p>|`-52`|
|{$STREAM.URL}|<p>We check the correctness of the URL used for the streaming stream</p>|``|
|{$SYSTEM.FUZZYTIME.MAX}|<p>The threshold for difference of system time in seconds.</p>|`60`|
|{$TEMP_CRIT_CPU}|<p>Critical CPU temperature in Celsius in case of overheating</p>|`95`|
|{$TEMP_CRIT_LOW_CPU}|<p>Critical CPU temperature in Celsius at low values</p>|`5`|
|{$TEMP_WARN_CPU}|<p>Critical CPU temperature in Celsius  in case of overheating but only WARN</p>|`85`|
|{$TUNER_FREQ}|<p>Checking the correctness of the tuner and MPX settings used</p>|`0`|
