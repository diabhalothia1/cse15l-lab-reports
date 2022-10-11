<img width="980" alt="Screen Shot 2022-09-28 at 4 22 51 PM" src="https://user-images.githubusercontent.com/100493743/193379673-0e013378-9650-45b9-bac4-f44b0f817650.png">
Go to the Visual Studio website  https://code.visualstudio.com/,, and download the version depending on the system youa re using, I downloaded the system
needed for MAC OS. 
<img width="627" alt="Screen Shot 2022-10-11 at 12 52 02 AM" src="https://user-images.githubusercontent.com/100493743/195030747-9c84ee92-8d76-4726-bf56-1d0d277535c0.png">
<img width="900" alt="Screen Shot 2022-10-11 at 12 31 49 AM" src="https://user-images.githubusercontent.com/100493743/195024155-27d8a1d1-f470-4a09-96c6-ec30ba9436e6.png">

I set up by cse15l account before the second lab so for this revison Im using that account, I logged using the ssh command and entered my password to login
Command-ssh cs15lfazz@ieng6.ucsd.edu
where zz is unique depending on your username
<img width="775" alt="Screen Shot 2022-10-11 at 12 35 32 AM" src="https://user-images.githubusercontent.com/100493743/195024874-2bf53fda-a36c-4f9f-8fb0-27d0e39a2916.png">

I tried multiple commands on my ssh account such as cd ~, cd, las
<img width="733" alt="Screen Shot 2022-10-11 at 12 36 08 AM" src="https://user-images.githubusercontent.com/100493743/195024999-80410e02-8102-42d6-8beb-5da1b71cbd02.png">
Some other commands i tried were-
~ cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/
~ cat /home/linux/ieng6/cs15lfa22/public/hello.txt
<img width="909" alt="Screen Shot 2022-10-11 at 12 47 32 AM" src="https://user-images.githubusercontent.com/100493743/195028925-0c5d7888-a802-4b02-9384-592e44a6e666.png">
<img width="486" alt="Screen Shot 2022-10-11 at 12 50 12 AM" src="https://user-images.githubusercontent.com/100493743/195030025-41b3ea26-e843-4db6-a52f-d7f3dfb5b566.png">
I had java installed in my sytem already, so I first ran the program and that what I got as my output. 
<img width="924" alt="Screen Shot 2022-10-11 at 12 48 02 AM" src="https://user-images.githubusercontent.com/100493743/195029152-aaa1d23c-6909-48d5-8bd3-acd36f91d42b.png">
I used the scp command and then logged usingg ssh and then after typing in the ls command I tried running the program I got a different output from the last time
The command was scp WhereAmI.java xxxx@ieng6.ucsd.edu:~/
<img width="799" alt="Screen Shot 2022-09-30 at 8 19 29 PM" src="https://user-images.githubusercontent.com/100493743/193384485-460e5aaa-3bc8-4f2b-952f-0c3fa321998d.png">

<img width="802" alt="Screen Shot 2022-09-30 at 8 15 10 PM" src="https://user-images.githubusercontent.com/100493743/193384374-819d1ac4-0a32-4b6e-a4bd-f272cc9ec8d3.png"><img width="785" alt="Screen Shot 2022-09-30 at 8 17 41 PM" src="https://user-images.githubusercontent.com/100493743/193384426-a08c454d-ef6e-4a28-87a7-ec963cce529e.png">

In this step the second time while loging in I didnt have to add my password , I follwed the following commands-
ssh-keygen
ssh xxxx@ieng6.ucsd.edu:
mkdir .ssh
<logout>
login again
then the command
ssh dbhalothia@ieng6.ucsd.edu "ls"
