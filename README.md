# bandit-over-the-wire

bandit_over_the_wire task

level 1 to 0 :
trerminal : 
           ssh bandit0@bandit.labs.overthewire.org -p 2220  
            ls
            cat readme --> password : boJ9jbbUNNfktd78OOpsqOltutMc3MY1
Learnt : ls --> to show all files 
         cat --> to show what is in the file


bandit 1 to 2:
terminal :      
          ssh bandit1@bandit.labs.overthewire.org -p 2220  
          ls
          cat<- --> password : CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
Learnt : how to open "-" files using cat in terminal


bandit 2 to 3:
terminal :
          ssh bandit1@bandit.labs.overthewire.org -p 2220
          cat "spaces in filename" --> UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
Learnt : how to open files using cat with spaces


bandit 3 to bandit 4:
terminal:
         ls --> inhere
         cd inhere
         ls -a  
         cat <.hidden -->pIwrPrtPN36QITSp3EQaw936yaFoFgAB
Learnt : how to open hidden files.


bandit 4 to bandit 5:
terminal:
         ls --> inhere
         cd inhere
         file ./*
         file07 --> ascii text
         cat ./-file07
Learnt : how to open ascii files  using cat


bandit 5 to bandit 6:
terminal:
         find -type f -size 1033c ! -executable
         cd maybehere07
         cat .file2 --> DXjZPULLxYr17uwoI01bNLQbtFemEgo7
Learnt : how to find a file of specific type


bandit 6 to bandit 7:
terminal:
          find / -user bandit7 -group bandit6 -size 33c 2>&1 | grep -F -v Permission | grep -F -v directory
          cat /var/lib/dpkg/info/bandit7.password -->HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
Learnt : how to open a file of specific type


bandit 7 to 8:
terminal:
          ls --> data.txt
          cat data.txt | grep millionth --> millionth cvX2JJa4CFALtqS87jk27qwqGhBM9plV
Learnt : how to grep(find anything specific in a file and piping)


bandit 8 to 9:
terminal:
         ls --> data.txt
         cat data.txt | sort | uniq -c -u -->  UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
Learnt : uniq -c ,uniq -u,sorting


bandit 9 to 10:
terminal:
        ls --> data.txt
        strings data.txt | grep ====  --> &========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
Learnt : conbert a file into and greping the file


bandit 10 to 11:
terminal:
        ls --> data.txt
        cat data.txt -->VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
        cat data.txt | base64 -d --> IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
Learnt : decode a base64 text


bandit 11 to 12:
terminal:
        ls --> data.txt
        cat data.txt --> Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
        alias rot13='tr a-zA-Z n-za-mN-ZA-M'
        cat data.txt | rot13 --> The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
Learnt : rotation of letter in alphabetical order.


bandit 12 to 13:
terminal:
        



























            
