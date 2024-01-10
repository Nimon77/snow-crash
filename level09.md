# level09

- `./level09 token`
    > tpmhr

- The output is arg[i]+i so we need to do a reverse program
```c
#include <unistd.h>

int main()
{
    int i = 0;
    char c;
    while(read(STDIN_FILENO, &c, 1) > 0)
    {
        putchar(c-i);
        i++;
    }
}
```

- When we run `cat token | a.out`
    > f3iji1ju5yuevaus41q1afiuq

- `$ su flag09` && `$ getflag`
    > Check flag.Here is your token : s5cAJpM8ev6XHw998pRWG728z

