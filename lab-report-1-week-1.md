<img width="980" alt="Screen Shot 2022-09-28 at 4 22 51 PM" src="https://user-images.githubusercontent.com/100493743/193379673-0e013378-9650-45b9-bac4-f44b0f817650.png">
Go to the Visual Studio website  https://code.visualstudio.com/,, and download the version depending on the system youa re using, I downloaded the system
needed for MAC OS. 
<img width="900" alt="Screen Shot 2022-10-11 at 12 31 49 AM" src="https://user-images.githubusercontent.com/100493743/195024155-27d8a1d1-f470-4a09-96c6-ec30ba9436e6.png">

I set up by cse15l account before the second lab so for this revison Im using that account, I logged using the ssh command and entered my password to login
Command-ssh cs15lfazz@ieng6.ucsd.edu
where zz is unique depending on your username
<img width="873" alt="Screen Shot 2022-09-30 at 7 38 35 PM" src="https://user-images.githubusercontent.com/100493743/193379878-f90c2e0e-a4e7-4988-a4d5-6cbb7b010655.png">
I tried multiple commands on my ssh account such as cd~, cd, las
Some other commands i tried were-
cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/
cat /home/linux/ieng6/cs15lfa22/public/hello.txt<img width="781" alt="Screen Shot 2022-09-30 at 7 44 06 PM" src="https://user-images.githubusercontent.com/100493743/193380037-629134bf-f31d-4522-8ce6-de0cf29a19fe.png">
I had java installed my sytem so I first ran the file WhereAmI.java using that then I used the scp command and tried again I got the same output both the times
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
