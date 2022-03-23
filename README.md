# Lab9

The program is about implementing fort() child and parents processes with signal handling. 

1) Initially we take the arguments from command line arguments and check for the possible possible errors. 
2) If arguments count from the command line argument is less than 2, we print the message on the terminal to check for the inputs and to enter the correct amount of inputs. 
3) Next we create the process by calling fork() function and assing the return value of the fork() function to process if variable "pid"
4) if the process id is equal to zero than it is called child process, if the process id is greater than zero than it is called parent process. 
5) In the child process we call the execvp funtion on first value in argv, and give the process size 1000
6) It will take some time to complete the above process, when we click control-c or control-z the process should be interupted, when the process is interepted we print that the child process didn't terminated normally. 
7) Than we go in the parent process using if statement if pid>0 and ignore the signals control-c and control-z and wait for the child process to terminate. 
8) If the child process is terminated the parent process wait for the signal control-\ to quit from the process. 
9) It the parent process receives control-\ it will call the singal_usr function for any errors if there are no errors it goes to signalquit and takes the input from the user to wheather exit from the process or not. 
10) if the answet is Y and parent process is exited. 

