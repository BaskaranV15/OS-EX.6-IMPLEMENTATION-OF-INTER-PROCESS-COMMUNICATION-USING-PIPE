# OS-EX.6-IMPLEMENTATION-OF-INTER-PROCESS-COMMUNICATION-USING-PIPE

## AIM:
To implement interprocess communication using pipe command.

## ALGORITHM:
1.Start

2.Create a child and parent using fork()

3.Allow communication between both the process

4.Stop

## PROGRAM:
```
#include <stdio.h>
int main()
{
int fd[2],child; char a[10];
printf("\n Enter the string:");
scanf("%s",a);
pipe(fd);
child=fork();
if(!child)
{
close(fd[0]);
write(fd[1],a,5); wait(0);
}
else
{
close(fd[1]);
read(fd[0],a,5); printf("The string received from pipe is: %s",a);
}
return 0;
}
```
## OUTPUT:

![image](https://github.com/BaskaranV15/OS-EX.6-IMPLEMENTATION-OF-INTER-PROCESS-COMMUNICATION-USING-PIPE/assets/118703522/a891fe14-cf2e-432f-9a9d-391e2e3729e3)


# RESULT:
 THUS THE IMPLEMENTATION-OF-INTER-PROCESS-COMMUNICATION-USING-PIPE WAS DONE SUCESSFUL
