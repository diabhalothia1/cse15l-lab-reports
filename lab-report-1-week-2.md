'import java.io.IOException;
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
