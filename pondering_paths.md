# Pondering Paths 
In this module I came across Linux File Paths. The Linux filesystem can be visuavalised as a "tree", every filesystem has a root which is represented using '/'. The root of filesystem is a directory within which there are other directories and files. Files and directories are refered using their paths. 

## The Root
In this level I invoked the program on the vscode workspace terminal to get the flag using '/pwn'. This style of path can be considered as the absolute path. It starts with root directory. 

<img width="342" alt="image" src="https://github.com/user-attachments/assets/33245fdd-59a3-4511-b3e3-c4a357ebc8c9">

## Program and absolute paths
In this level I invoked the challenge directory in which all the challenges of pwn.college reside. I invoked /challenge/run to execute the run file that is in the challenge directory whose root is / on the vscode workspace terminal to get my flag which I submitted.

<img width="391" alt="image" src="https://github.com/user-attachments/assets/ea2beb65-25b9-443e-abbe-e4ba18811b73">

## Position thy self
In this level, I learnt that you can navigate through directories using the cd (change directory) command, this affects the "current working directory". The '~' symbol the current shell you're working in. In the terminal I first ran /challenge/run program which was prompted as incorrect and showed me the path to the correct directory (/var/log). Seeing that I changed to that directory using the cd command and then ran the /challenge/run program which was indeed correct and I was awarded my flag as it was invoked from the right directory.

<img width="425" alt="image" src="https://github.com/user-attachments/assets/4e614bcb-d9db-40fa-943c-e7c85695983c">

## Position elsewhere
In this level, I used the concepts learnt in the previous lesson i.e., changing directories using cd. Hence, I solved this level in a similar manner. This time the right directory was /usr/share/doc/fontconfig. I changed my directory to that using cd and then ran the /challenge/run program and I got my flag.

<img width="432" alt="image" src="https://github.com/user-attachments/assets/55f299f9-7e0e-4416-97c5-c1566bc16336">

## Position yet elsewhere
This level was similar to the last two levels and naturally I followed the same line of action as I did previously. This time the right directory was /usr/include and I recieved the flag when I ran the absolute path i.e., /challenge/run after changing into that directory. 

<img width="407" alt="image" src="https://github.com/user-attachments/assets/361fccf9-01db-44d3-b22c-df4bd56a8ec5">

## Implicit relative paths, from /
In this level, I was familiarised with relative paths. Relative paths don't start with a root (no '/') and are intpreted relative to your current working directory. So, in this level I was asked to run /challenge/run using a relative path while having current working directory of '/'. At first, I was stuck for a bit. Later it dawned upon me I must first change my directory to '/' and then run the run it using its relative path that is challenge/run. This was correct and I got my flag.

<img width="388" alt="image" src="https://github.com/user-attachments/assets/6f498d75-2832-4931-998b-958699413821">

## Explicit relative paths, from /
I learnt that in the previous level, the relative path was naked. Every directory has two implicit entries that you can reference in paths: '.' and '..'. Absolute paths can be represented multiple ways using them and so can relative paths however there is no presence of a root ('/') in the relative path. Now, in this level I first changed the directory to '/' using cd command and then used the relative path ./challenge/run in the next prompt that was right and I got my flag.

<img width="409" alt="image" src="https://github.com/user-attachments/assets/df9d51ae-6fae-49bc-a2c1-78684f62af43">

## Implicit relative path
In this level, I first changed my directory to /challege using cd command. Since I cannot invoke my /challenge/run in it's naked form for safety reasons, I ran, 'run' using it's relative path explicitly i.e., ./run hence avoiding the conflict.

<img width="343" alt="image" src="https://github.com/user-attachments/assets/659cf6df-7e01-4171-8eaa-aa555a34dcf0">

## Home sweet home
The goal of this level was to specify a file as an argument on the command line along with /challenge/run. So, I wrote entered ~/f along with /challenge/run to complete this challenge. The idea was to create a file inside /home/hacker (~) directory that will be written by /challenge/run. So I created a file 'f' which resides in /home/hacker and its absolute path is ~/f.

<img width="338" alt="image" src="https://github.com/user-attachments/assets/f684e7b9-70a5-4361-b5dc-8f221b158660">





