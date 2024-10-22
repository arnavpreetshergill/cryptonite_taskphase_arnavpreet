# MAtching with * 
#### When * is used in a command, the system treats it as a ""wild card" or a "blank" and returns whatever file or program fits this "blank"
## Solution: 
```
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{UKQwKbaaPA6xlcPCBmeH2cn_mZH.dFjM4QDL3EDN3czW}
```
# Matching with ?
#### ? is similar to *, but it only acts like a blank for a single character
## Solution: 
```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8tpofdJ9JcZ8jTWLCAXziaonS5f.dJjM4QDL3EDN3czW}
```
# Matching with []
