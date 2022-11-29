PART 1

Task-
Changing the name of the start parameter and its uses to base

Code to change all start paramaters-


```
:%s/start/base/g<Enter>:w!<Enter>

```
  
 <img width="797" alt="Screen Shot 2022-11-29 at 3 31 26 PM" src="https://user-images.githubusercontent.com/100493743/204672048-32f01211-936b-4982-a35a-d3d54274cfe1.png">

<img width="907" alt="Screen Shot 2022-11-29 at 3 31 40 PM" src="https://user-images.githubusercontent.com/100493743/204672080-55af6e35-5a92-47e8-83dd-6437e38abad1.png">

<img width="881" alt="Screen Shot 2022-11-29 at 3 31 53 PM" src="https://user-images.githubusercontent.com/100493743/204672109-73cb3835-980d-4512-a4b3-0615b277ba31.png">

<img width="923" alt="Screen Shot 2022-11-29 at 3 32 01 PM" src="https://user-images.githubusercontent.com/100493743/204672145-de34e635-cd0a-4152-81c5-c457f2429599.png">



 Explanation of vim code-
  
  :s is used to substute a certain word in the file with another word
  
  :%s goes through entire file looking for the work to be subsituted 
  
  /g substitues all the appearences of that word in the entire file
  
  :w is used to save the changes into the file
  
  How does the file look after running those vim commands-
  <img width="591" alt="Screen Shot 2022-11-14 at 9 05 37 AM" src="https://user-images.githubusercontent.com/100493743/201723079-26615077-d9fc-4b3c-b8f1-fcf1284923db.png">
  
<img width="844" alt="Screen Shot 2022-11-14 at 9 05 45 AM" src="https://user-images.githubusercontent.com/100493743/201723087-47bdf24e-9037-439a-82ee-63cae87f327e.png">
  
 PART 2
  
  
 Making the edit the first way-10 mins
  
 Making the edit second way-15 mins , I was stuck for a bit on running the tests on the ssh server and making the dit took more time
  
  I would prefer working the first way beacuse I feel more comfortable making the edit first and then running the file on the remote server by scp the file , whereas on the ssh login I felt it was a little more hard because it took me more time and I felt it hard to understand where I was going wrong
  
  I would prefer scp the file and running on the remote server but if i have a file on multiple servers and I want it change in all of them, I would prefer taking the second option and making the edit on the remote server and running it there.
