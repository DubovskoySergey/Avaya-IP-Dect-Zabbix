<h1>Zabbix template for monitoring radio stations Avaya IP Dect Base Station</h2>

This template has been tested on Avaya IPBS2-C3-1B1 devices with IP Dect R4 v10p2p9 and Zabbix 6.0 firmware.

To use it, import the template to your Zabbix server and change the values in the macros to your own:<br>
<b>{$DECT.PASS}<br>
{$DECT.USER}<br>
{$SNMP_COMMUNITY}</b>

To do this, you need to know the login and password from the base stations, as well as specify the Community Name in the base stations themselves.

The template implements monitoring of the current state of the "State" base stations. Base stations have 3 states:<br>
<b>Master</b> - if the base station is a master;<br>
<b>Synchronized</b> - if the base station is in sync with other stations;<br>
<b>Unsynchronized</b> - if the base station has lost synchronization.

The current status is received once every 1 minute, if for some reason zabbix receives an Unsynchronized status from the base station, a trigger will trigger and you will see this event in the list of problems.

