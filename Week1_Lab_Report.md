# Remote access


## Installing VScode
- To install VScode, go to https://code.visualstudio.com/ and download the version suitable for your personal laptop or computer. I downloaded a version for macOS.
- After downloading, you can access the terminal and customize the color themes. It was a lot of fun changing the themes! I used Dark High Contrast.
- When you open VScode, it should look something like this. <img width="1512" alt="Screen Shot 2023-01-12 at 10 17 57 AM" src="https://user-images.githubusercontent.com/114725358/212421023-ba0dd28f-17b9-47ab-8cfd-535686fb9798.png">

## Remotely Connecting (for macOS)
- Press  **_Control + `_** together to open a new terminal. 
- To use ssh, enter the given command and replace abc with your specific account for this course.
  > (_Pro tip_: In the tutorial, there was a $ added in front of the same command. I added it to my command at first. I finally understood that it was a part of the terminal but on my terminal it looks like \~. So, if you have \$ or \~ showing on the terminal, enter the given command.) 
   
                                                  sshcs15lwi23abc@ieng6.ucsd.edu  
- It asks if you want to connect or not, type “yes”. Then, enter your password for the course.<img width="685" alt="Screen Shot 2023-01-13 at 1 45 21 PM" src="https://user-images.githubusercontent.com/114725358/212425024-0d4b165a-a296-46b4-9540-922f6da03f89.png">
- After this, you would get the following message:<img width="715" alt="Screen Shot 2023-01-13 at 1 47 55 PM" src="https://user-images.githubusercontent.com/114725358/212425377-93cdd6e9-5c64-44f8-a429-c6e50a3f7772.png">
- You should be logged in and able to remotely access the server.

## Trying Some Commands
- Once logged in, try the following commands: cd, ls, pwd, cat, cp etc.
- One of the things I tried to do was move back a directory and try to access some other users accounts but it just said “Permission denied” as it should have!
- Here is an example:  <img width="1007" alt="Screen Shot 2023-01-12 at 12 48 50 PM" src="https://user-images.githubusercontent.com/114725358/212425873-2efc6a98-b78f-4136-910c-dbfd5861ba77.png">  <img width="1094" alt="Screen Shot 2023-01-12 at 12 49 27 PM" src="https://user-images.githubusercontent.com/114725358/212425926-1d31695c-424e-4ba9-bc16-8401c9aa7b18.png">  <img width="1087" alt="Screen Shot 2023-01-12 at 12 49 43 PM" src="https://user-images.githubusercontent.com/114725358/212426119-b7bcfd60-c0a4-4976-bc85-0df450f1ae70.png">  
- To exit, press **_Control + D_** together or type **_exit_** on the command line. 
- Try different combinations of commands!


