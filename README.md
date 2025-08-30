# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:


# PROGRAM:

## C Program to create new process using Linux API system calls fork() and getpid() , getppid() and to print process ID and parent Process ID using Linux API systeM CALL

#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{
//variable to store calling function's process id
pid_t process_id;
//variable to store parent function's process id
pid_t p_process_id;
//getpid() - will return process id of calling function
process_id = getpid();
//getppid() - will return process id of parent function
p_process_id = getppid();
//printing the process ids
//printing the process ids
printf("The process id: %d\n",process_id);
printf("The process id of parent function: %d\n",p_process_id);
return 0;
}
#OUTPUT

<img width="746" height="492" alt="Screenshot 2025-08-30 192108" src="https://github.com/user-attachments/assets/8b55293b-d030-4a8d-a8be-fba58383e49f" />





C Program to create new process usingLinux API system calls fork() and exit()

#include <stdio.h>
#include<stdlib.h>
int main()
{ int pid;
pid=fork();
if(pid == 0)
{ printf("Iam child my pid is %d\n",getpid());
printf("My parent pid is:%d\n",getppid());
exit(0); }
else{
printf("I am parent, my pid is %d\n",getpid());
sleep(100);
exit(0);}
}
#OUTPUT


<img width="747" height="189" alt="Screenshot 2025-08-30 192538" src="https://github.com/user-attachments/assets/aa46961e-f87c-46ac-9500-81783fd9e8d7" />


## C Program to execute Linux system commands using Linux API system calls exec() , exit() , wait() family
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
printf("Running ps with execlp\n");
execlp("ps", "ps", "ax", NULL);
printf("Done.\n");
exit(0);
}

























##OUTPUT

<img width="752" height="208" alt="Screenshot 2025-08-30 192549" src="https://github.com/user-attachments/assets/925f45e2-36d5-4139-a8a4-1352ece0d87c" />


















# RESULT:
The programs are executed successfully.
