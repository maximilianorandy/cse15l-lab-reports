Lab 2 - Week 1

[Week 1 – Remote Access and the Filesystem](https://ucsd-cse15l-f22.github.io/week/week1/)

So for this lab there was a problem with everyones account and we could not log into our online servers, but my partner reset his password 2 days prior so we where able to do it on his account. As of right now I have tried multiple times an hour to see if it works, but it still does not work. So I will not be using screen shots for my lab report because I can not obtain them.

## Installing VScode
First you will need to download Visual Studio Code on your computer and to do that you should go to this [link](https://code.visualstudio.com/)
Once you have downloaded it, then it should look like the picture below.

![week 1 lab](https://user-images.githubusercontent.com/66755589/193378429-4e348244-e4c5-4c7b-9ab1-0e45f0ea01f7.png)

## Remotely Connecting
Second you will need to connect to the server remotely. To start off that process you will need to open up the terminal and you do that by clicking the button at the top that says terminal and then click new terminal. Next we must type in ssh into the terminal and then press space and then your user name it starts off with `cs15lfa22` then you enter your special two letters then follow it up by typing `@ieng6.ucsd.edu` with no spaces inbetween. Once you do that and press enter you will then be prompted to enter your password which should work when you enter it.

![photo Lab 1 #2](https://user-images.githubusercontent.com/66755589/195947507-d12b8d1d-0f87-4ea8-afa2-5088ca3be87a.png)

![photo Lab 1 #3](https://user-images.githubusercontent.com/66755589/195947627-3b85be8e-f1a1-4812-b076-cfcd6f4ded8f.png)

## Trying Some Commands
The third thing you need to do is to enter into the terminal different commands for example to enter the `cd` command you are changing the command directory. When you do `ls -a` it prints out a list of the files in a block format and in `ls -lat` it lists the files with one on each line.

![photo Lab 1 #4](https://user-images.githubusercontent.com/66755589/195947998-fbe1a69c-67d0-418a-af73-cab3ffc22778.png)

## Moving Files with scp
The fourth thing you need to do is to be in your client and to type `scp` and then enter the name of the file you need to transfer which in this case is WhereAmI.java which holds the code below:

![photo Lab 1 #1](https://user-images.githubusercontent.com/66755589/195941854-7c9194c8-c549-482a-a35f-b92de0136435.png)

Then write your user name again with this at the end `:~/` we type this at the end to tell the computer that we are done with that section and we could even type a different file name to change its name. It will then prompt you for your password and once you enter it, the name of the file you transferred will be written there.

## Setting an SSH Key
So to set up an "SSH Key" you need to then run the command `ssh-keygen` and then that will give you a file called a public key and a private key which you will then store into two seperate places. You will need to store the purblic key into the .ssh directoy.

## Optimizing Remote Running
To do this you will need to write the regular log in and then at the end instead of pressing enter you will write in quotation marks. The command you want to run in the remote server will then run once you press enter, it will run because you are sending a message from the client to the server.
