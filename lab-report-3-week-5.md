
The command I'm going to explore is <span style="color: red;">GREP</span> 

1. -n

Example of using -n

  1. It gives the line number in which a particular word is contained in a file

  The code for using -n to get the line number of lines conatining that keyword-
  
        grep -n "keyword" <file>
  
  I used this to find the appearence of "unknown" in the file "chapter-1.txt"
  
  
 <img width="720" alt="Screen Shot 2022-11-11 at 2 02 21 PM" src="https://user-images.githubusercontent.com/100493743/201440008-0a77db25-4531-4b17-beed-403b76bbe3a6.png">

  2.You can use this file to search a keyword through multiple files and get line numbers in all these l files which contain that keyowrd
  
   The code for using -n to get the line number of lines conatining that keyword-  
  
          grep -n "keyword" <file>
  
   I used this to find the appearence of "unprecented" in all the files of government
  
 <img width="775" alt="Screen Shot 2022-11-11 at 2 30 57 PM" src="https://user-images.githubusercontent.com/100493743/201439901-d0bee16c-754f-451c-8857-76e365f54915.png">
  
  
  3.You can use this command to find all the digits in a file
  
  The code for using -n to get the line number of lines containing that keyword-
  
    grep -n "^[[:digits:]]" <file>
  
  I used this to find the digits in Mitchell-Mit.txt 
  

<img width="815" alt="Screen Shot 2022-11-11 at 2 50 25 PM" src="https://user-images.githubusercontent.com/100493743/201447234-c9a39c4a-bc8e-4e34-8be2-86d20a99bc02.png">


2.-r

Examples of using -r

1. You can find all the files in a directory that have a specific pattern 
  
  The code to use -r to get a specific pattern in a dirctory 
  
      grep -r "pattern" <directory>
      
  I used this to find "hours" in the directory 911 report

  
  
  <img width="1440" alt="Screen Shot 2022-11-11 at 4 33 20 PM" src="https://user-images.githubusercontent.com/100493743/201449779-c1113cca-2a32-4a3c-856c-1e695829b530.png">


2.You can even find a pattern in a larger directrory with other directories and the files in them

The code to use -r to get a specific pattern in a dirctory 
  
      grep -r "pattern" <directory>
      
I used this to find "largely" in technical
This not only give me other directories but also the files in those directories that contain largely

<img width="1015" alt="Screen Shot 2022-11-11 at 5 31 46 PM" src="https://user-images.githubusercontent.com/100493743/201453018-dfa24d9d-fc42-467a-80d2-57855faaa88a.png">

<img width="1011" alt="Screen Shot 2022-11-11 at 5 37 26 PM" src="https://user-images.githubusercontent.com/100493743/201453023-0d436b6d-02d4-4b76-b3e9-6b8ae965f48b.png">

<img width="1031" alt="Screen Shot 2022-11-11 at 5 38 56 PM" src="https://user-images.githubusercontent.com/100493743/201453059-0bb4284c-2fe1-4cf6-ab77-a7d7aa01eb64.png">

3.We can use it with the -i command to ingore the case sensitivty and find the papptern in all the files in a directory

The code to use -r to get a specific pattern in a dirctory 
  
      grep -r -i "pattern" <directory>
      
I used this to find "UNKNOWN" in technical

<img width="1440" alt="Screen Shot 2022-11-11 at 6 53 31 PM" src="https://user-images.githubusercontent.com/100493743/201453322-387cf902-1c6c-4935-814c-6456125b8618.png">


