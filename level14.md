# level14

- This time we have nothing, the last thing we can do is disassemble `getflag`

- With ghidra we can see 2 blocking problems
    - We check if we are in a decompiler with ptrace so we need to bypass that
    - The uid get by getuid need to be the one from flag14

- 1st thing `ptrace` is store in `eax` register at `0x08048989` we need to change it

- 2nd thing `getuid` is store in `eax` register at `0x08048afd` we need to change it too
    ```gdb
    (gdb) b *0x0804898e
    (gdb) b *0x08048b0a
    (gdb) r
    Starting program: /bin/getflag 

    Breakpoint 1, 0x0804898e in main ()
    (gdb) info registers 
    eax            0xffffffff	-1
    [...]
    (gdb) set $eax=0
    (gdb) c
    Continuing.

    Breakpoint 2, 0x08048b0a in main ()
    (gdb) info registers 
    eax            0x7de	2014
    (gdb) set $eax=3014
    (gdb) c
    Continuing.
    Check flag.Here is your token : 7QiHafiNa3HVozsaXkawuYrTstxbpABHD8CPnHJ
    [Inferior 1 (process 2180) exited normally]
    ```
