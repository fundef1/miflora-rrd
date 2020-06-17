# miflora-rrd
Openwrt oriented shell script for Xiami Miflora plant sensor

Meant to run as a daily cronjob,\
fetches (historic) data from Xiaomi Miflora sensor.\
uses gatttool for talke BLE to the sensor and rrdtool(1) to store readings and create graphs

still needs clean-up, but usable nonetheless ;-)\
Mainly checking momentary values instead of historic values: no bulk read is possibly anyway, so no (power) benefit in reading the history.

The script (gatttool) assumes the BT-dongle to be 'up'.\
do ```/usr/bin/hciconfig hci0 up``` before calling ```miflora-rrd```\
(or just add that line to /etc/rc.local)

You can get values for your plants here: 
https://raw.githubusercontent.com/khronimo/MiFloraDB/master/PlantDB_5335_U0.csv

