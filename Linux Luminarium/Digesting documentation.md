# Challenges 
## Learning from documentation 
#### In this challenge, all we need to do is pass a simple argument in the /challenge/challenge program to get the flag. By using '--giveflag' and an additonal argument of '/flag', the flag is acquired.
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag /flag 
Correct argument! Here is your flag:
pwn.college{g9X2ws5gAvIHdr-oTPWi3XPpvD-.dRjM5QDL3EDN3czW}
```
## Learning Complex usage
#### Similar to previous challenge, simply replace '--giveflag' with '--printfile'
```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{M4IQlpPv6fPq2HAfvI2NCSHCDd7.dVjM5QDL3EDN3czW}
```
## Reading manuals
#### This challenge deals with the 'man' command, which returns the manual of the command given as an argument
```
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                                                             Challenge Commands                                                                             CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --fhhtby NUM
              print the flag if NUM is 534

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                                                                   May 2024                                                                                  CHALLENGE(1)
hacker@man~reading-manuals:~$ /challenge/challenge --fhhtby 534
Correct usage! Your flag: pwn.college{Af5hY3htb4Gy1SdZh1uBoT9mTkm.dRTM4QDL3EDN3czW}
```
## Searching manuals
#### '/' can be used to search manuals, and '?' can be used to search manuals backwards
#### n to move to next occurance and N to move backwards
#### for this challenge, just run the command
```
man challenge
```
#### this returns the manual which has a lot of useless arguments. just search for 'flag' which will give us the corrent argument whhich is '--rre'
```
hacker@man~searching-manuals:~$ /challenge/challenge --rre
Initializing...
Correct usage! Your flag: pwn.college{waXqLQtrff9yWNnqjlv_KL9ZzXq.dVTM4QDL3EDN3czW}
```
## Searching for manuals
#### this challenge involves using the 'man man' command, which returns a detailed manual about the man command. after this, it can be seen that '-k' can be used to search, so simply run this command:
```
hacker@man~searching-for-manuals:~$ man -k challenge
xfkipznryy (1)       - print the flag!
```
then run this: 
```
hacker@man~searching-for-manuals:~$ man xfkipznryy

CHALLENGE(1)                                                                             Challenge Commands                                                                             CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --xfkipz NUM
              print the flag if NUM is 343

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college 
```
and finally: 
```
hacker@man~searching-for-manuals:~$ /challenge/challenge --xfkipz 343
Correct usage! Your flag: pwn.college{U3xTfQkiYpznCrFyyPCTTFcqk-G.dZTM4QDL3EDN3czW}
```
## Helpful programs
#### just use -h 
```
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 28
hacker@man~helpful-programs:~$ /challenge/challenge -g 28
Correct usage! Your flag: pwn.college{spdI0swT2J8UoY1LUu-MGIcQe1A.ddjM4QDL3EDN3czW}
```
## Help for Builtins 
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "4apCIT8n".
hacker@man~help-for-builtins:~$ challenge --secret 4apCIT8n
Correct! Here is your flag!
pwn.college{4apCIT8naaDC-64zzTWApHNxkrh.dRTM5QDL3EDN3czW}
```
