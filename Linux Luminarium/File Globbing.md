# Matching with * 
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
#### [] will only return the files that match the characters enclosed within the braces.
## Solution:
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{wjrmi6zkpPfHRjXoAKtN58b50No.dNjM4QDL3EDN3czW}
```
# Matching paths with []
#### globbing using [] also works for absolute paths
## Solution: 
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{0ZfHQmSYXMOIT5_eQCWTlUUpqwg.dRjM4QDL3EDN3czW}
```
# Mixed Globbing
#### Since we know the starting letter of each word, we can use a [] and then * to narrow down to the required files 
## Solution: 
```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{InUy2ELbTOy3SjrNqnc66N7kM3H.dVjM4QDL3EDN3czW}
```
# Exclusionary Globbing
#### ! or ^ can be used as the first character in [] to exclude the proceeding characters from the glob
## Solution: 
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
'hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{4iZRNvTtPrxjeZdRIuGSjqH36KB.dZjM4QDL3EDN3czW}
```
