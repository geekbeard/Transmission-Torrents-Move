Transmission-Torrents-Move
==========================

**Transmission Torrents Move Script**


A small script which you can put in cron job to run every N minutes and check the status of the torrents in progress and move them to a specific folder upon completion.

**Usage:**

1) download mt2.sh and put it to any folder you'd like
2) you should make sure your Transmission torrents has authentication set and the user with password.
3) open mt2.sh with nano for example: `$ nano mt2.sh`
4) change first three variables:

`MOVEDIR=`  - the folder to move completed downloads to
`USERNAME=` - transmission authentication username
`PASSWORD=` - transmission authentication password

5) after filling in this information exit nano by `CTRL+X` and typing `Y + Enter`
6) You can now already test the script by executing it `$ ./mt2.sh` or `$ sudo ./mt2.sh`

Setting a cronjob(root):

`$ sudo crontab -e` - open cron jobs for root user.
add line `*/5 * * * * /path/to/mt2.sh` - change `/path/to/` to the path where you have mt2.sh. also you can change `*/5` to indicate another interval in minutes. change 5 to 10 minutes or higher (or less) to run this script every N minutes.

Now it's done! Enjoy)

p.s. It is very easy to add e-mail notifications to this script. 
