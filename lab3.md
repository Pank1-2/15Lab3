# CSE 15l Lab Report 3 - Kiko Pan 

The command that I will be researching further in lab report 3 is the ```find``` command. 

## Method 1 ```-name```

One way you can use the ```find``` command is with the ```-name``` option. ```find``` is used to locate files and directories. Adding the ```-name``` option along with find command finds the specific file name path. For example, running ```find . -name chapter-1.txt``` searches the current directory for a file that matches the file name given after the ```-name```. It then returns the path that matches the file name and if there isn't anything that matches, it returns nothing. This is useful when we want to find the path of a specific file or find the path of files that end in .txt or .pdf.
<p align="center"> <img src = "Screen Shot 2023-05-09 at 2.49.09 PM.png" width = "550" height = "50"> </p>

Another way to use this option within the ```find``` command is searching for files based on their extension. You can add * in replace of the name of the file and do ```"*.txt"``` to search for all files that end with a .txt. In the image below, I ran the following command: ```find . -name "*.txt"```. 

<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.32.02 PM.png" width = "300" height = "450"> </p>

[Source](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)

## Method 2 ```-size```

Another useful way to use ```find``` is with ```-size```. The ```-size``` option allows you to find files or directories greater than or less than a certain size. In the example below, I run the follwing command: ```find . -type f -size -10M``` and it lists all the files in the current directory that is less than 10MB. This is useful when you want to search for files based on their size. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.16.57 PM.png" width = "300" height = "490"> </p>

Another way of using ```-size``` would be to find the files that are greater than a certain size. You can do this by running ``` find . -type f size +1M```. As you can see in the image below, none of the files in the current technical directory is greater than 1MB. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.29.51 PM.png" width = "550" height = "50"> </p>

[Source](https://geekflare.com/linux-find-commands/)

## Method 3 ```-mtime```

The ```find``` command is also useful when we want to see when a file was last modified, accessed, or created. We can use ```-mtime``` to find the files last modified within a certain time frame. ```ctime``` can be used to find the files created within the time frame given and ```atime``` can give the files that were accessed within the time frame. For example if we wanted to find the files modified within the past 2 days, we can run the following command: ```find . -type f -mtime -2```. As you can see in the image below, there were no files that were modified within the last 2 days. The ```-time``` option is useful when we want to find files based on when they were modified. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.47.04 PM.png" width = "550" height = "50"> </p>

Similarly, if we wanted to find the files that were created within the last two days, we can run ``find . -type f -ctime +2```. This command looks into the current directory and finds all the files that were created within the past 2 days. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 4.50.09 PM.png" width = "300" height = "450"> </p>

[Source](https://linuxhandbook.com/find-command-examples/)

## Method 4 ```-exec```

You can also use multiple find option together. For example, you can use the ```-name``` with ```-exec```. A command you can run while combining multiple find options would be ```find . -name "*.txt" -exec echo {} \;```. This command finds all the files that end in .txt and executes echo on the file. The {} represents the file that was found and the \; indicates the end of the command. Below is an image of this command ran in the technical directory. The ```-exec``` option is useful if we wanted to execute certain actions on specific files that were found by find. 
<p align="center"> <img src = "Screen Shot 2023-05-09 at 5.58.45 PM.png" width = "300" height = "450"> </p>

Another way you can use the ```-exec``` is by combining it with ```grep``` as well. For example you can run the following command: ```find . -name "*.txt" -exec grep "chapter" {} \;```. This command finds all the files ending with .txt and executes the grep command that takes in a keyword which in this case is 'chapter'. This will print out the contents of the files that contain the keyword chapter. 

<p align="center"> <img src = "Screen Shot 2023-05-09 at 6.05.57 PM.png" width = "450" height = "450"> </p>

[Source](https://www.baeldung.com/linux/find-exec-command)




