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
