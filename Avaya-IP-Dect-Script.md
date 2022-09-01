Sometimes, after the loss of synchronization, the base stations do not recover on their own. To restore synchronization, a reboot of the base station is required. I simplified the process of rebooting the base station by writing a script that Zabbxi sends a GET request to the problematic base station to reboot it.<br>
The script below:<br>
<i>curl -u {$DECT.USER}:{$DECT.PASS} -k 'https://{HOST.CONN}/CMD0/mod_cmd.xml?cmd=reset&xsl=reset.xsl&reset=OK'</i>

