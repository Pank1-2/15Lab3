# CSE 15l Lab Report 3 - Kiko Pan 

The command that I will be researching further in lab report 3 is the ```find``` command. 

1. One way you can use the ```find``` command is with the ```-name``` option. ```find``` is used to locate files and directories. Adding the ```-name``` command along with find searches for the specific file name path. For example, running ```find . -name chapter-1.txt``` searches the current directory for a file that matches the file name given after the ```-name```. It then returns the path that matches the file name and if there isn't anything that matches, it returns nothing.
<p align="center"> <img src = "Screen Shot 2023-05-09 at 2.49.09 PM.png" width = "550" height = "50"> </p>
Another way to use this command is searching for files based on their extension. You can add * in replace of the name of the file and do ```"*.txt" to search for all files that end with a .txt. In the image below, I ran the following command: ```find . -name "*.txt"```. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.16.57 PM.png" width = "300" height = "450"> </p>

Source: https://www.tecmint.com/35-practical-examples-of-linux-find-command/

2. Another useful way to use ```find``` is with ```-size```. The ```-size``` option allows you to find files or directories greater than or less than a certain size. In the example below, I run the follwing command: ```find . -type f -size -10M``` and it lists all the files in the current directory that is less than 10MB. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.16.57 PM.png" width = "300" height = "450"> </p>
Another way of using ```-size``` would be to find the files that are greater than a certain size. You can do this by running ``` find . -type f size +1M```. As you can see in the image below, none of the files in the current technical directory is greater than 1MB. 
 
 Source: https://geekflare.com/linux-find-commands/

3. 



