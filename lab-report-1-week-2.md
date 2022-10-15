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
  
  Everytime I run the code this list is reset and losses its orginal values and I can add new Values again
  
  <img width="500" alt="Screen Shot 2022-10-14 at 8 46 43 PM" src="https://user-images.githubusercontent.com/100493743/195967451-57ed45da-1fb4-4811-b6e4-f142e3b7d69b.png">
 
  The second screenshot shows the search Menthod, in this screenshot I have search 'app' in my oringinal list and got the elements that had 'app' in them
  
  For this we can only run this method along with the pp query cause we close the webserver after running the add query when we open the server again it will have an empty list
  
  Part 2
  File-ArrayExample
  Method-ReverseInPlace
  
  
  Test That failed Output
  
  
  @Test 
	public void testReverseInPlace1() {
    int[] input2={3,4,5};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{ 5,4,3 }, input2);
  }
  
  
  Symptom/ Wrong Output
  
  -5,4,5
  
  The bug
  
  static void reverseInPlace(int[] arr) {
    int[] Parameter =arr;
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = Parameter[arr.length - i - 1];
    }
  }
  
  
  We were making changes to the oringinal code, so after running the method first time the original list got changes and thus, the output was wrong
  I fixed the bug by creating a copy of the original list and instead of referencing the orginal list I refernced the copy, and thus we will get the right output.
  
  
  File-ListExamples.java
  Method-merge
  
 Test That failed Output
 All the test will run the program but none would pass the test
 
 Symptom: The program is stuck in infite loop
 
  <img width="298" alt="Screen Shot 2022-10-14 at 9 05 23 PM" src="https://user-images.githubusercontent.com/100493743/195967974-c91bf232-14ca-4f3c-b952-9e34cf8de02d.png">
  
  
This, index 2 will always be smaller than the size of list 2

Bug


<img width="398" alt="Screen Shot 2022-10-14 at 9 06 07 PM" src="https://user-images.githubusercontent.com/100493743/195967989-15570def-8175-4e85-85bc-299cec1de7f3.png">

Incrementing the value of index 2 in the second loop so that eventually the while loop terminates. 
