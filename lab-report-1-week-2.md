`import java.io.IOException;
import java.net.URI;
import java.util.*; 

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    List<String> s = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().contains("/add")) 
        { 
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                s.add(parameters[1]);
                for(String nw:s){
                    return s.toString();
                }
            }
        
        }
        else if (url.getPath().contains("/search")) 
        { 
            String[] parameters1 = url.getQuery().split("=");
            if (parameters1[0].equals("s")) {
                List<String> s1 = new ArrayList<>();
                
                for(String nw:s){
                    if(nw.contains(parameters1[1])){
                        s1.add(nw);
                    }
                     
                }
                return s1.toString();
            }
        
        }
        return "404 Not Found!";
    }
}

class SearchEngine {
    public static void main(String[] args) throws IOException {
    
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());

    
    }
}`
  <img width="397" alt="Screen Shot 2022-10-14 at 8 41 13 PM" src="https://user-images.githubusercontent.com/100493743/195967353-af6c11ca-ab57-4869-95a5-67f528aa4e8c.png">

  This screenshot is for the first part-the add method of the code, it shows all the things I added to the list by using the add query
  
  The first step checks that if the url contains /add and then it splits the query by looking for the '=' sign in an array
  
  Then it checks if the first elements of array created by the quesry is s and if that is true if adds the second element from the array created by the query to a new array.
  
  Then using a for loop all elements of s are returned in a string format.
  
  Everytime I run the code this list is reset and losses its orginal values and sets an empty list and I can add new Values again
  
  <img width="500" alt="Screen Shot 2022-10-14 at 8 46 43 PM" src="https://user-images.githubusercontent.com/100493743/195967451-57ed45da-1fb4-4811-b6e4-f142e3b7d69b.png">
  
  
 
  The second screenshot shows the search Method, in this screenshot I have search 'app' in my original list and got the elements that had 'app' in them
  
  The first step checks that if the url contains /search and then it splits the query by looking for the '=' sign in an array
  
  Then it checks if the first elements of array created by the query is s and if that is true it goes into a for loop iternating through the array created by the add method, then it checks if the array contains the element in the array created by the query, if it does the element is added to the new array created by us
  
  After iternating through the for loop it returns the new array by converting it to a string
  
  For this we can only run this method along with the add query cause if we close the webserver after running the add query when we open the server again it will have an empty list
  
  Part 2
  
  
  File-ArrayExample
  Method-ReverseInPlace
  
  
  Test That failed Output
  
  
 <img width="538" alt="Screen Shot 2022-10-27 at 1 40 30 PM" src="https://user-images.githubusercontent.com/100493743/198393505-403a989c-fd3d-4ef8-a50f-c03785bf8f8a.png">

  
  Symptom/ Wrong Output
  
  -<img width="915" alt="Screen Shot 2022-10-27 at 1 41 44 PM" src="https://user-images.githubusercontent.com/100493743/198393716-c8f8407b-0cfc-4203-9762-83d5ca35af55.png">

  
  The bug
  

  <img width="530" alt="Screen Shot 2022-10-27 at 1 42 49 PM" src="https://user-images.githubusercontent.com/100493743/198393916-cae90de7-3139-4284-8230-5ae817ebd507.png">

  
  
  We were making changes to the original code, so after running the method first time the original list got changes and thus, the output was wrong
  I fixed the bug by creating a copy of the original list and instead of referencing the orginal list I refernced the copy, and thus we will get the right output.
  
  
  File-ListExamples.java
  
  Method-merge
  
 Test That failed Output
 
 <img width="1016" alt="Screen Shot 2022-10-28 at 3 53 57 PM" src="https://user-images.githubusercontent.com/100493743/198747829-c017817d-9fe7-4908-a406-b31fdfbc7a8c.png">


 Symptom: The program is stuck in infite loop
 
  <img width="298" alt="Screen Shot 2022-10-14 at 9 05 23 PM" src="https://user-images.githubusercontent.com/100493743/195967974-c91bf232-14ca-4f3c-b952-9e34cf8de02d.png">
  
  
  <img width="617" alt="Screen Shot 2022-10-28 at 3 52 33 PM" src="https://user-images.githubusercontent.com/100493743/198747784-7150d883-5438-4d52-999d-bffe08283432.png">

  
This, index 2 will always be smaller than the size of list 2

Bug


<img width="398" alt="Screen Shot 2022-10-14 at 9 06 07 PM" src="https://user-images.githubusercontent.com/100493743/195967989-15570def-8175-4e85-85bc-299cec1de7f3.png">

Incrementing the value of index 2 in the second loop so that eventually the while loop terminates. 
