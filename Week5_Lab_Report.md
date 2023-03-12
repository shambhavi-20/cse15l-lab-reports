# Tasks
- I forked [the lab 7 repository](https://github.com/ucsd-cse15l-w23/lab7) as a part of setup.
 
 <img width="800" alt="Screen Shot 2023-02-23 at 11 20 49 PM" src="https://user-images.githubusercontent.com/114725358/221116892-83291f06-bec9-4590-89c7-3cb97cf82af2.png">

- Log into ieng6: I did not have to put in my password because I set up a SSH Key for my ieng6 account from my local computer. 

```
Keys pressed: <up><enter> 

The [ ssh cs15lwi23aqe@ieng6.ucsd.edu ] command was 1 up in the search history, 
so I used the up arrow to access it. 
After that, I just pressed Enter to log in to my ieng6 server.
```
<img width="1045" alt="Screen Shot 2023-02-23 at 11 21 58 PM" src="https://user-images.githubusercontent.com/114725358/221117311-ce7c7f00-6ec7-4e56-982b-ecbec3e87e33.png">
<img width="993" alt="Screen Shot 2023-02-23 at 11 22 10 PM" src="https://user-images.githubusercontent.com/114725358/221117320-4b61c95c-faf7-4b0f-a27c-7abd90b66ffb.png">

- Create a bash script to make the rest of the process faster.
```
Keys pressed: <nano tasks.sh><enter> 

The [ nano tasks.sh ] creates a new new nash file.
```
<img width="650" alt="Screen Shot 2023-03-11 at 4 32 58 PM" src="https://user-images.githubusercontent.com/114725358/224517740-e718325c-2fc4-47dd-ad61-13fd30efc32a.png">
<img width="1044" alt="Screen Shot 2023-03-11 at 4 31 26 PM" src="https://user-images.githubusercontent.com/114725358/224517697-c25ab6cd-a59b-4d5b-9a0c-c5c443f1eb39.png">

For all the tasks below, I copy pasted the commanads i knew worked into the bash script.
- Clone your fork of the repository from your Github account.
- Run the tests, demonstrating that they fail. 
- Edit the code file to fix the failing test.
- Commit and push the resulting change to your Github account.
``` 
I pasted the following commads:
git clone https://github.com/shambhavi-20/lab7
cd lab7/
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar 
org.junit.runner.JUnitCore ListExamplesTests
nano ListExamples.java 

echo "changes made to ListExamples.java"

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar 
org.junit.runner.JUnitCore ListExamplesTests
git add ListExamples.java
git commit -m "updated"

Keys pressed: <Ctrl-O><enter><Ctrl-X>  

I put [ echo "changes made to ListExamples.java" ] to notify
that changes have been made to "ListExamples.java".
The rest of the commands were copied from Lab reoprt 4 and 
pasted into the bash script. 
```
<img width="1029" alt="Screen Shot 2023-03-11 at 4 39 50 PM" src="https://user-images.githubusercontent.com/114725358/224517965-6d444fdd-ac1d-452d-b036-1e2a944c0135.png">

- To run all the commands
```
Keys pressed: <bash t><tab><enter>, 
I used [ bash tasks.sh ] command to rull the commands indoe the bash file. 
I used tab to autocomplete tasks.sh and then Enter.

```
<img width="507" alt="Screen Shot 2023-03-11 at 4 45 08 PM" src="https://user-images.githubusercontent.com/114725358/224518126-eb2c1f4b-bc9e-4e30-9e26-3b86a94bce63.png">


- The bash opens the nano terminal after cloning the repository and running the tests.
```
Keys pressed:  
<Ctrl-W><result.ad><enter><Ctrl-E><left side><left side><left side>
<delete><delete><delete>, 
<scroll down to last the while><down><down><right side><right side><right side>
<right side><right side><right side><right side><right side><delete<2>, 
<Ctrl-O><enter><Ctrl-X>   

Then I used various ways to navigate through the file to change the errors.
I used Ctrl-W to search for result.add.
Then, I used Ctrl-E to get to the end of the line and moved left to delete "0, ".
Then I scrolled down with my touchpad and used the right key to move. 
I changed "index1" to "index2". I used Ctrl-O and Enter to save the changes. 
Finally, I pressed Ctrl-X to exit from nano.
```
<img width="1030" alt="Screen Shot 2023-03-11 at 4 49 05 PM" src="https://user-images.githubusercontent.com/114725358/224518188-291acdcb-e353-49d2-8ea1-121353435e94.png">



- After that it runs the test again and commits the changes to github.
- the whole output looks like this:


  <img width="776" alt="Screen Shot 2023-03-11 at 4 47 15 PM" src="https://user-images.githubusercontent.com/114725358/224518152-0bccc929-7344-4177-9381-47606f5ad477.png">



