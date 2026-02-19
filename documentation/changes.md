## Versioning
The versioning received an update because the logic in it was nowhere to be found. It is now based on:<br>
- [YY].[M].[#] [Release type]<br>
- Example: 26.2.1 stable<br>

***

## Changes

### Changes in version 26.2.1 stable compared to 25.x stable
<ins>HUGE changes:</ins></br>
- Gave the project a name. Meet: "HeishaMoNR"
- Added support for **zone 2** (rewrite)
- Added support for **buffer tank** (rewrite)
- Added generic **MQTT-command manager** functionality. It checks if commands are picked up by the Panasonic. If not it retries 3x


<ins>Big changes:</ins></br>
- WAR renamed to CCC. (from Dutch WeersAfhankelijkeRegeling to CustomCompensationCurve, which makes more sense)</br>
- Added a MQTT-command rate limiter to prevent/reduce panasonic dropping commands</br>
- Added zone 2 support to CCC function</br>
- Added zone 2 support to RTC function</br>
- RTC Automations require a single target zone</br>
- Added support for P1 meters which reports different data types. (type 1 / 2)</br>
- Added extra external Link-In options. See right side of [WP Input]-tab. 

<ins>Other noteworthy changes:</ins></br>
- SoftStart function rewrite to accomodate for buffertank and multizone setups</br>
- Improved charts. Now surviving reboots</br>
- Allow sending HEAT setpoints in all operating modes</br>
- Removed all QOS 1 and 2 on mqtt nodes. It is not supported</br>
- Added more Panasonic pump versions to detect</br>
- Fan 2 auto-show/hide when it is detected</br>

<ins>Existing limitations:</ins></br>
- Cool function only works in DIRECT mode. (still on the list to fix, but is on low priority)
  
[Back](../readme.md)

***

### Changes in v25.00 compared to v24.03 stable
<u>Major changes:</u></br>
- Firmware Support: Added compatibility with Heishamon Firmware 3.9</br>
- SoftStart function rewrite: now with improved relax frequency and TCAP recognition</br>
- Scheduler Enhancements: Added more actions</br>
- Scheduler Enhancements: Added more advanced conditions (room/outside temperature thresholds)</br>
- Sensors: Added extra 1-wire sensor support to show in graphs of DHW, HEAT, and ROOM temps</br>
</br>

SoftStart function:</br>
- SoftStart Fixes: Resolved bugs related to defrost phase and startup loops</br>
</br>

<u>RTC function:</u></br>
- Multiple improvements to prevent premature triggering</br>
- Multiple improvements for the reverting actions</br>
- MQTT Fixes: Eliminated repeating commands like SetZ1CoolRequestTemperature</br>
</br>

<u>Charts & UI Improvements:</u></br>
- Home screen: If Fan2 is present, it will show up (and stay) after first value enters.</br>
- Home screen: Added Heater, it will show up (and stay) after first value enters. And when active, it will light up.</br>
- Translated some chart labels from Dutch to English</br>
</br>

<u>Solar²DHW:</u></br>
- Forced DHW-only mode during a run for better compatibility with HEAT+DHW</br>
- Improved kWh calculations and graph visuals</br>
- More robust energy tracking in Solar²DHW (fixed NaNs, graph is now more robust, but could increase loading a bit)</br>
- Moved P1 setup to [SYSTEM] > [SENSORS] tab. Much better.</br>
</br>

Miscellaneous Fixes:</br>
- Reading Panasonic details logic rewritten for fw3.9</br>
- Powerful mode toggle fix</br>
- Pressure readout (TOP115) added</br>

