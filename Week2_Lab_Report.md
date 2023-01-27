# Part 1 - Web Server


## a) Code for StringServer.java
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // adding a message after every search query.
    ArrayList<String> data = new ArrayList<String>();
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Shambhavi's String displayer");
        } 
        
        else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s") ) {
                    data.add(parameters[1]);
                    String result="";
                    for (int i=0; i<data.size(); i++){
                        result+="\n"+data.get(i);
                    }
                    return result;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

```
## b) Screenshots of the  web server using /add-message

<img width="611" alt="Screen Shot 2023-01-27 at 12 30 24 PM" src="https://user-images.githubusercontent.com/114725358/215191245-14d4fb46-626f-464f-82c8-a37f5b641770.png">
<img width="574" alt="Screen Shot 2023-01-27 at 12 34 23 PM" src="https://user-images.githubusercontent.com/114725358/215191743-ff2c37b2-7fd9-4a48-96e5-2e337951e53c.png">
- Which methods in your code are called? StringServer has the main method which is being used to create the server. Then, to handle 
- 
What are the relevant arguments to those methods, and the values of any relevant fields of the class?
How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.





# Part 2 - Bugs and Symptoms
- An choosing the bug in reversed of ArrayExamples.java
- A failure inducing input is {1,2,3}:
```
  @Test
  public void testReverse1() {
    int[] input1 = {1,2,3};
    int[] output = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[]{3,2,1}, output);
  }
```
We expect {3,2,1}, but get {0,0,0}.

- A non-failure inducing input is {0}:
```
  @Test
  public void testReversed() {
    int[] input1 = {0};
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input1));
  }
  ```
  We get what we expect.
  
- In both testReverse1 and testReverse2, the symptom is very similar. Because we are updating arr with a newly created array newArray, the method is always return an array with its elements as 0. 
<img width="1133" alt="Screen Shot 2023-01-27 at 1 51 45 PM" src="https://user-images.githubusercontent.com/114725358/215208609-96d09ebc-9f96-43bb-8241-d26a37c3508f.png"><img width="1132" alt="Screen Shot 2023-01-27 at 1 51 13 PM" src="https://user-images.githubusercontent.com/114725358/215208647-30e05ec8-7d71-4622-a5dc-3f4af3938aac.png">


