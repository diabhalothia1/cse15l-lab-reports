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


<img width="943" alt="Screen Shot 2022-10-11 at 12 15 51 PM" src="https://user-images.githubusercontent.com/100493743/195179409-9cb52702-b75b-4af6-b127-2f537f9f560d.png">
<img width="630" alt="Screen Shot 2022-10-11 at 12 16 05 PM" src="https://user-images.githubusercontent.com/100493743/195179461-61739254-aa23-45f4-8153-5cd5b2990291.png">
<img width="946" alt="Screen Shot 2022-10-11 at 12 35 00 PM" src="https://user-images.githubusercontent.com/100493743/195182767-f7845b6d-51c9-4a9b-b8e8-6c17da5b0dc2.png">

In this I succesfully logged into my ssh login without entering the password
First I used the ssh-keygen command to create a key for my password
After that using the ssh login mkdir. ssh and exit commands and using the spc command we make this key copy public
After that as you can see I logged in using ssh cs15lfa22xx@ieng6.ucsd.edu without needing to enter the password


<img width="935" alt="Screen Shot 2022-10-12 at 3 59 17 PM" src="https://user-images.githubusercontent.com/100493743/195472783-8cfb2772-9071-43e2-887c-f1e9cb597e2d.png">


I added another print statemnt saying "My name is dia"
Then I copied the file using scp, ssh and javac and java command all in one line to save time from running and got the above output
Which is same output as original WhereAmI.java + my name is dia
