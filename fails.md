
So for this lab there was a problem with everyones account and we could not log into our online servers, but my partner reset his password 2 days prior so we where able to do it on his account. As of right now I have tried multiple times an hour to see if it works, but it still does not work. So I will be using my partners screen shots for right now, but when the reset finishes I will change the screen shots. My partner that I worked with in the lab was Rui Li.


## Part 3
Picture of my log into VS code
![week 1 lab](https://user-images.githubusercontent.com/66755589/193355198-540f3c1e-11dd-4392-b20e-9a46b1bf9d7b.png)


## Part 4
This is the text that came out when we got into the servers. The key differences between what we got and the examples from the lab instructions was the numbers in the cluster status. Another detail that was different is that ours did not say `quota: No filesystem specified`. The difference could mean that there is more people on the remote server when we where using it.
![accessing the servers](https://user-images.githubusercontent.com/66755589/193355928-64c45387-d694-4267-a17b-b543c9b76f8b.png)


## Part 5
Me and my partner did the commands that where listed for us to do but out of those the most intresting ones to me where `ls -lat` and `ls -a` and you can see below that they both give the same information of what files are there. The only difference is that `ls -lat` displays all of the files in a long list with each file getting its own line, while for `ls -a` the files are all condenced into a easy to read block with multiple files per line.
![command imputs](https://user-images.githubusercontent.com/66755589/193358320-6043b362-e1a2-4def-8bc9-d3165e67c765.png)


## Part 6
In the photo below we are transfering the file from the client to the server. We do this by typeing scp and then the file name and then we write where we are sending it to which is cse15lfa22ev@ieng6.ucsd.edu and then at the end we write ":~/" to signify that its the end of the line. It then prompts us for our password again and once we submit it then it prints out the name of the file we sent.
![trasnfering  the file](https://user-images.githubusercontent.com/66755589/193362817-e8c09f3f-da09-4994-b86b-cbbbcf1c3429.jpg)

*Q1: What’s different about the output when you run this on the client vs. the server? What does this mean for what getProperty does?*

A1: When we run in client and server, the WhereAmI file outputs the OS, username, and the path where we are. The information that they give off is different, in the client the OS is windows 10, username is rul043, but in the server the OS is linux and the username is cs15lfa22fc. The last key difference is the paths that show where the file was taken from. This means that for getProperty is a method in java that can get the current user information.(This answer was done by me and my partner Rui Li)

*Q2: How long did it take you? (Not everyone has to do this, but someone should.) Assume you’d have to do this process 100 times over the course of a PA. How long would you spend copying and running the file?*

A2: It took Rui 30 seconds to copy the file from the client to the server and run it, while for me it took about 2 minutes because I am a very slow typer and it was my first time. I would proboly take about 75 minutes on copying and running the file because I would eventually get the hang of it.

## Part 7
