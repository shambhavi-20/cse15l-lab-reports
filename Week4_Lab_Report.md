# Tasks
- I forked [the lab 7 repository](https://github.com/ucsd-cse15l-w23/lab7) as a part of setup.<img width="800" alt="Screen Shot 2023-02-23 at 11 20 49 PM" src="https://user-images.githubusercontent.com/114725358/221116892-83291f06-bec9-4590-89c7-3cb97cf82af2.png">

- Log into ieng6: I did not have to put in my password because I have set up a SSH Keys for my ieng6 account.

```
Keys pressed: <up><enter> 

The ssh cs15lwi23aqe@ieng6.ucsd.edu command was 1 up in the search history, so I used up arrow to access it. 
```
<img width="1045" alt="Screen Shot 2023-02-23 at 11 21 58 PM" src="https://user-images.githubusercontent.com/114725358/221117311-ce7c7f00-6ec7-4e56-982b-ecbec3e87e33.png">
<img width="993" alt="Screen Shot 2023-02-23 at 11 22 10 PM" src="https://user-images.githubusercontent.com/114725358/221117320-4b61c95c-faf7-4b0f-a27c-7abd90b66ffb.png">


- Clone your fork of the repository from your Github account.

```
Keys pressed: <Ctrl-R><git clo><enter> 

The git clone https://github.com/shambhavi-20/lab7 command was very far up in the search history. 
So, I used Ctrl-R to search for it. I typed "git clo" and found the command. After that I just pressed Enter.
```
<img width="604" alt="Screen Shot 2023-02-24 at 4 00 22 AM" src="https://user-images.githubusercontent.com/114725358/221174113-02b4a76c-012c-40e2-9980-d7691b5ecc29.png">

- Run the tests, demonstrating that they fail.
```
Keys pressed: <cd la><tab><enter>, <Ctrl-R><javac><enter>, <Ctrl-R><java -c><enter>

I used cd lab7/ command to get into the required files.
The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was very far up in the search history. 
So, I used Ctrl-R to search for it. I typed "javac" and found the command. After that I just pressed Enter.
The java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples command was far up in the search history. 
So, I used Ctrl-R to search for it. I typed "java -c" and found the command. After that I just pressed Enter. The output shows that one test is failing.
```
<img width="957" alt="Screen Shot 2023-02-24 at 4 18 57 AM" src="https://user-images.githubusercontent.com/114725358/221180215-dad030f9-ab47-4888-b946-9de0e3a4ff14.png">

- Edit the code file to fix the failing test.
```
Keys pressed: <nano Li><tab><j><tab><enter>, <Ctrl-W><result.ad><enter><Ctrl-E><left side><left side><left side><delete><delete><delete>, <scroll down to last the while><down><down><right side><right side><right side><right side><right side><right side><right side><right side><delete<2>, <Ctrl-o><enter><Ctrl-x>   

I used nano ListExamples.java to edit the file.
Then i used various . 



```
<img width="515" alt="Screen Shot 2023-02-24 at 4 34 24 AM" src="https://user-images.githubusercontent.com/114725358/221180275-90ed6141-ee58-4520-8aee-2d70eefb7c6f.png">
- Run the tests, demonstrating that they now succeed.
Keys pressed: <cd la><tab><enter>, <Ctrl-R><javac><enter>, <Ctrl-R><java -c><enter>

I used cd lab7/ command to get into the required files.
The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was very far up in the search history. 
So, I used Ctrl-R to search for it. I typed "javac" and found the command. After that I just pressed Enter.
The java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples command was far up in the search history. 
So, I used Ctrl-R to search for it. I typed "java -c" and found the command. After that I just pressed Enter. The output shows that one test is failing.
```
Commit and push the resulting change to your Github account
