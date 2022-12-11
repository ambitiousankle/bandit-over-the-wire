# bandit-over-the-wire

bandit_over_the_wire task

## bandit0 0 :
           ssh --> secure shell

## bandit 0 to 1 :
#### trerminal : 
           ssh bandit0@bandit.labs.overthewire.org -p 2220  
            ls
            cat readme --> password : NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
#### Learnt :
           ls --> to show all files 
           cat --> to show what is in the file


## bandit 1 to 2:
#### terminal :      
          ssh bandit1@bandit.labs.overthewire.org -p 2220  
          ls
          cat<- --> password : rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
#### Learnt :
           how to open "-" files using cat in terminal


## bandit 2 to 3:
#### terminal :
          ssh bandit2@bandit.labs.overthewire.org -p 2220
          cat "spaces in filename" --> aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
#### Learnt :
           how to open files using cat with spaces


## bandit 3 to bandit 4:
#### terminal:
         ssh bandit3@bandit.labs.overthewire.org -p 2220  
         ls --> inhere
         cd inhere
         ls -a  
         cat <.hidden --> 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
#### Learnt : 
           how to open hidden files.


## bandit 4 to bandit 5:
#### terminal:
         ssh bandit4@bandit.labs.overthewire.org -p 2220  
         ls --> inhere
         cd inhere
         file ./*
         file07 --> ascii text
         cat ./-file07 --> lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
#### Learnt : 
           how to open ascii files  using cat


## bandit 5 to bandit 6:
#### terminal:
         ssh bandit5@bandit.labs.overthewire.org -p 2220  
         find -type f -size 1033c ! -executable
         cd maybehere07
         cat .file2 --> P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
#### Learnt :
           how to find a file of specific type


## bandit 6 to bandit 7:
#### terminal:
          ssh bandit6@bandit.labs.overthewire.org -p 2220 
          find / -user bandit7 -group bandit6 -size 33c 2>&1 | grep -F -v Permission | grep -F -v directory
          cat /var/lib/dpkg/info/bandit7.password --> z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
#### Learnt :
           how to open a file of specific type


## bandit 7 to 8:
#### terminal:
          ssh bandit7@bandit.labs.overthewire.org -p 2220 
          ls --> data.txt
          cat data.txt | grep millionth --> millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP
#### Learnt :
           how to grep(find anything specific in a file ) and piping.


## bandit 8 to 9:
#### terminal:
         ssh bandit8@bandit.labs.overthewire.org -p 2220  
         ls --> data.txt
         cat data.txt | sort | uniq -c -u -->  EN632PlfYiZbn3PhVK3XOGSlNInNE00t
#### Learnt : 
           uniq -c (count the number of unique files)
           uniq -u (show the unique files)
           sort (sort lines to text)


## bandit 9 to 10:
#### terminal:
        ssh bandit9@bandit.labs.overthewire.org -p 2220
        ls --> data.txt
        strings data.txt | grep ====  --> &========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
#### Learnt : 
           convert a file into and greping the file


## bandit 10 to 11:
#### terminal:
        ssh bandit10@bandit.labs.overthewire.org -p 2220   
        ls --> data.txt
        cat data.txt --> VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
        cat data.txt | base64 -d --> 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
#### Learnt :
           decode a base64 text.


## bandit 11 to 12:
#### terminal:
        ssh bandit11@bandit.labs.overthewire.org -p 2220   
        ls --> data.txt
        cat data.txt --> Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
        alias rot13='tr a-zA-Z n-za-mN-ZA-M'
        cat data.txt | rot13 --> The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
#### Learnt : 
           rotation of letter in alphabetical order.


bandit 12 to 13:
terminal:
        ssh bandit12@bandit.labs.overthewire.org -p 2220   
        ls --> data.txt
        mkdir /tmp/break
        cp data.txt /tmp/break
        cd /tmp/break
        ls --> data.txt
        cat data.txt
        
        cat data.txt | xxd -r > data
        file data --> data: gzip compressed data, was "data2.bin"
        
        mv data data2.gz
        gzip -d data2.gz
        ls --> data2 
        file data2 --> data: bzip2 compressed data, block size = 900k
        
        mv data2 data3.bz
        bzip2 -d data3.bz
        ls --> data3
        file data3 --> data3: gzip compressed data
        
        mv data3 data4.gz
        gzip -d data4.gz
        ls --> data4
        file data4 --> data4: POSIX tar archive 
        
        mv data4 data5.tar
        tar -xf data5.tar
        ls --> data5.bin
        file data.bin
        data5.bin: POSIX tar archive 
        
        mv data5.bin data6.tar
        tar -xf data6.tar
        ls --> data6.bin
        file data6.bin
        data6.bin: bzip2 compressed data, block size = 900k
        
        mv data6.bin data7.bz
        bzip2 -d data7.bz
        ls --> data7
        file data7
        data7: POSIX tar archive 
        
        mv data7 data8.tar
        tar -xf data8.tar
        ls --> data8.bin
        file data8.bin --> data8.bin: gzip compressed data
        
        mv data8.bin data9.gz
        gzip -d data9.gz
        ls --> data9
        file data9 --> ascii text
        cat data9 --> wbWdiBxEir4CE81aPhauu0o6pwRmrDw
        
        
        

         



























            
