Sometimes, after the loss of synchronization, the base stations do not recover on their own. To restore synchronization, a reboot of the base station is required. I simplified the process of rebooting the base station by writing a script that Zabbxi sends a GET request to the problematic base station to reboot it.<br>
The script below:<br>

![image](https://user-images.githubusercontent.com/34303263/187914782-5b845d63-e2b6-4a7d-b308-87ecebbff1eb.png)


<i>curl -u {$DECT.USER}:{$DECT.PASS} -k 'https://{HOST.CONN}/CMD0/mod_cmd.xml?cmd=reset&xsl=reset.xsl&reset=OK'</i>

![image](https://user-images.githubusercontent.com/34303263/187914959-728002cd-fe4a-4a39-9105-4cf4a94d6efa.png)
