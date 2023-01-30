# Part 1 - Web Server


**a) Code for StringServer.java**

```ruby
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

**b) Screenshots of the  web server using /add-message**

<img width="611" alt="Screen Shot 2023-01-27 at 12 30 24 PM" src="https://user-images.githubusercontent.com/114725358/215191245-14d4fb46-626f-464f-82c8-a37f5b641770.png">
<img width="574" alt="Screen Shot 2023-01-27 at 12 34 23 PM" src="https://user-images.githubusercontent.com/114725358/215191743-ff2c37b2-7fd9-4a48-96e5-2e337951e53c.png">

- Class StringServer has the main method which is being used to create the server. StringServer takes the port number as the argument. Then, to handle the entered URL, handleRequest from the Handler class is called. The method takes the URL as its argument. 
- If the path of the URL is "/", the page displays "Shambhavi's String displayer". 
- If the path of the URL is "/add-message", the method checks for the query. If "s" is found in the query, the statement after "=" that could be a set of any characters (E.g. "abc", "123") is added to the instance variable data. Then, the method iterates over data and returns a String with all the previously added statements. 
- If all these steps are not satisfied, the server displays an error "404 Not Found!". 
- So, every time we reload the server, the variable URL changes and we get a different output based on the value conditions given above.



# Part 2 - Bugs and Symptoms

- I am choosing the bug in reversed of ArrayExamples.java (Returns a *new* array with all the elements of the input array in reversed order.).
- A failure inducing input is {1,2,3}. We expect {3,2,1}, but get {0,0,0}.

```Ruby
  @Test
  public void testReverse1() {
    int[] input1 = {1,2,3};
    int[] output = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[]{3,2,1}, output);
  }
```


- A non-failure inducing input is {0}. We get what we expect.

```Ruby
  @Test
  public void testReversed() {
    int[] input1 = {0};
    assertArrayEquals(new int[]{0}, ArrayExamples.reversed(input1));
  }
  ```
 
  
- In both testReverse1 and testReverse2, the symptom is very similar. Because we are updating arr with a newly created array newArray, the method willl always return an array with its elements as 0. 
<img width="1133" alt="Screen Shot 2023-01-27 at 1 51 45 PM" src="https://user-images.githubusercontent.com/114725358/215208609-96d09ebc-9f96-43bb-8241-d26a37c3508f.png"><img width="1132" alt="Screen Shot 2023-01-27 at 1 51 13 PM" src="https://user-images.githubusercontent.com/114725358/215208647-30e05ec8-7d71-4622-a5dc-3f4af3938aac.png">

- The code before the fix:
```
 // Returns a *new* array with all the elements of the input array in reversed order.
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
```
- The code after the fix:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        newArray[i] = arr[arr.length - i - 1]; //change
    }
    return newArray;//change
  }
```
- The code was updating the old array arr with the values of the new array newArray. So, I just interchanged the two and now the code is updating newArray.
- The code was returning arr instead of newArray. But we are asked to return a new array. So, I changed it to the return newArray. 

# Part 3

- Everything done in Lab 2 was new for me. It was fun learning how to create a web server. A web server sounded very ambitious at first but after I did it, the process was very rewarding. Committing changes to Gihub, cloning repositories to VS Code, and finally playing around with the server was very fun. Debugging is something I have done before but following the steps given really helped me. It made my understanding of the code and my efficiency in finding edge cases better.
