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
         
          

































            
