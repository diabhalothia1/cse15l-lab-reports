
The command I'm going to explore is <span style="color: red;">GREP</span> 

1. -n

Example of using -n

  1. It gives the line number in which a particular word is contained in a file

  The code for using -n to get the line number of lines conatining that keyword-
  
        grep -n "keyword" <file>
  
  I used this to find the appearence of "unknown" in the file "chapter-1.txt"
  
  
 <img width="720" alt="Screen Shot 2022-11-11 at 2 02 21 PM" src="https://user-images.githubusercontent.com/100493743/201440008-0a77db25-4531-4b17-beed-403b76bbe3a6.png">

  2.You can use this file to search a keyword through multiple files nad get line numbers in all these l=files which contain that keyowrd
  
   The code for using -n to get the line number of lines conatining that keyword-  
  
          grep -n "keyword" <file>
  
   I used this to find the apperaence of "unprecented" in all the files of government
  
 <img width="775" alt="Screen Shot 2022-11-11 at 2 30 57 PM" src="https://user-images.githubusercontent.com/100493743/201439901-d0bee16c-754f-451c-8857-76e365f54915.png">
  
  
  3.You can use this command to find all the digits in a file
  
  The code for using -n to get the line number of lines conatining that keyword-\
  
    grep -n "^[[:digits:]]" <file>
  
  I used this to find the digits in 
  

    <img width="815" alt="Screen Shot 2022-11-11 at 2 50 25 PM" src="https://user-images.githubusercontent.com/100493743/201441499-ffe626b3-1e01-4445-8d01-2881298712fe.png">

  
  
  
