PART 1

Task-
Changing the name of the start parameter and its uses to base

Code to change all start paramaters-

':%s/start/base/g<Enter>:w<Enter>
  
  
  <img width="145" alt="Screen Shot 2022-11-14 at 9 04 06 AM" src="https://user-images.githubusercontent.com/100493743/201722241-3b9bddf5-2110-4fe3-8bd7-543f87f3880f.png">
  
  
<img width="33" alt="Screen Shot 2022-11-14 at 9 05 10 AM" src="https://user-images.githubusercontent.com/100493743/201722255-da44437d-ea32-4f8c-9a69-4dbeea743fa1.png">

 Explanation of vim code-
  
  :s is used to substute a certain word in the file with another word
  
  :%s goes through entire file looking for the work to be subsituted and /g substitues all the appearences of that word in the entire file
  
  :w is used to save the changes into the file
  
  How does the file look after running those vim commands-
  <img width="591" alt="Screen Shot 2022-11-14 at 9 05 37 AM" src="https://user-images.githubusercontent.com/100493743/201723079-26615077-d9fc-4b3c-b8f1-fcf1284923db.png">
  
<img width="844" alt="Screen Shot 2022-11-14 at 9 05 45 AM" src="https://user-images.githubusercontent.com/100493743/201723087-47bdf24e-9037-439a-82ee-63cae87f327e.png">
  
  
 Making the edit the first way-10 mins
 Making teh edit second way-15 mins , I was stuck for a bit on ruuning the tests on the ssh server
  
  I would prefer working the first way beacuse I feel more comfortable working on the remote server and running the tests , whereas on the ssh login it ws a little more hard to undertand and I feel like that it was took me more time
  
  I would prefer scp the file wnd working on the remote server but if i have a file on multiple servers and I want it change in all of them, I would prefer taking the second option
