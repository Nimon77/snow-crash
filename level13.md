# level13

- If we disassemble level13 we can see that we put the result of getuid in a var,
    we can change this var between getuid and the `if` check with gdb

    `if` check is at `0x0804859a`
    ```gdb
    (gdb) b *0x0804859a
    (gdb) r
    (gdb) info registers
    eax            0x7dd	2013
    [...]
    (gdb) set $eax=4242
    (gdb) info registers
    eax            0x1092	4242
    [...]
    (gdb) c
    Continuing.
    your token is 2A31L79asukciNyi8uppkEuSx
    ```
    > Flag is 2A31L79asukciNyi8uppkEuSx    
