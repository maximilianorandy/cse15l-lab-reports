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
We will be useing WhereAmI.java and the code for it is seen as below:

![photo Lab 1 #1](https://user-images.githubusercontent.com/66755589/195941854-7c9194c8-c549-482a-a35f-b92de0136435.png)

We have to check if we have the code in the right folder before we send it so we type `javac WhereAmI.java` which complies the code and `java WhereAmI.java` which runs it then we know we have it and it is availible to send it to the server. You can see this demonstraited below.

![photo Lab 1 #5](https://user-images.githubusercontent.com/66755589/195962596-6cf73b4c-8947-4da0-8b10-2539510715ad.png)

So now to send it you need to be in your client terminal and to type `scp` and then enter the name of the file you need to transfer which in this case is `WhereAmI.java` . Then write your user name again with this at the end `:~/` we type this at the end to tell the computer that we are done with that section. It will then prompt you for your password and once you enter it, the name of the file you transferred will be written there.

![scp](https://user-images.githubusercontent.com/66755589/195962697-e4a9ed20-221d-43cf-8bd0-eecc96aeddc5.png)

We can then go into the server and see if the file is there by doing the `ls -a` and you can see below that the file from the computer is now on the server.

![photo Lab 1 #6](https://user-images.githubusercontent.com/66755589/195962755-83e41d80-b9f7-4131-b335-2f7b20c7b65d.png)

## Setting an SSH Key
So to set up a `SSH` we will need to be in the client terminal and we will need to write `ssh-keygen -t ed25519` and once we write that in there we press enter and it will ask to press a key so we use `enter` and then we will do it again to confirm it to the computer then it will generate a privte key and a public key. You will get the picture that loads onto your screen like the picture below and the private key will be store in the remote server, which is what we will do next

![creating key](https://user-images.githubusercontent.com/66755589/195964024-79521b57-a86f-4c47-99ad-b2ea19f4297e.png)

To store it in the remote server we must log in and type into the terminal mkdir .ssh and that will store the piece of the key in the server which will make it easier for us to open the server from our computer. We then log our of it then go to the client. there we will write our own personal path to tell the key where the other end it, the path I wrote for mine is 
"\Users\maxim/.ssh/id_ed25519.pub cs15lfa22ev@ieng6.ucsd.edu" that is my path your path can be seen before your cliet loads up the text image, then after that you write ":~/ssh/authorized_keys" to end off the line your writing with not spaces between the pieces. Once you press enter it should be done and it should work for you to just enter the ssh log in info then press enter and it will just go straight in.

## Optimizing Remote Running
To omtomize remote running we could set up the SSH key like we did above which makes it so much easier for us to log into the server from the client.

We could also type in terminal line after we write in our ssh log in info and put quotation marks what we would like to do in the server online. This is what I did in the picture below and in there I used `ls` to read me out the files

![oprtimizing remote running](https://user-images.githubusercontent.com/66755589/195964289-82ea2438-9070-48ad-b155-e725474bce78.png)
