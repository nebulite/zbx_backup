Current old-stable version

## Using of v0.4
### Version 0.4 is not development anymore
You must necessarily specify some variables on the top of the script:  
<b>DEST:</b> the place where we should store final archive.  
<b>TMP:</b> the script creates some temporary files and one of them is SQL backup folder. So, you must specify catalog of relevant size.  
<b>ROTATION:</b> How many old copies you want to hold.

Example:  
DEST=/mnt/nfs/zabbix  
TMP=/var/tmp/zbx_backup  
ROTATION=10  

For database backup v0.4 expects what you have innobackupex utility installed. Also, you must specify user for MySQL instance and his passoword. Password can be set plaintext or placed to some file, which content you can get with 'cat' utility.
Example:  
DB_USER="root"  
DB_PASS=`cat /root/.mysql`  
