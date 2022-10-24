Week 3 Lab

[Week 3 ](https://ucsd-cse15l-f22.github.io/week/week3/#week3-lab-report)

## Part 1

For this lab this week we focused on making our own search engine, the code for that search engine is below.

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> searching = new ArrayList<>();

    public String handleRequest(URI url) {
        String invalid = "Invalid input. Try again.";

        if (url.getPath().equals("/")) {
            String list = "";
            for (int i = 0; i < searching.size(); i++){
                list += searching.get(i) + "\n";
            }
            return "The current list contains: \n \n" + list;
        }
        
        else if (url.getPath().contains("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")){
                searching.add(parameters[1]);
                return parameters[1] + " item added";
            }
        } 

        else if (url.getPath().contains("/search")) {
            String[] parameters = url.getQuery().split("=");
            String done = "";
            if (parameters[0].equals("s")){
                for(int i = 0; i < searching.size(); i++){
                    if (searching.get(i).contains(parameters[1])) {
                        done += searching.get(i) + "\n"; 
                    }
                }
                if (done.equals("")){
                    return "No string passed.";
                }
                return done;
            }
            return invalid;
        } 
        return "404 Not Found!";
    }
}


class SearchEngine {
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

Default:

So to even start the website, to get to the default page you need to run the code first by compling it in the terminal with the command `javac Server.java SearchEngine.java` and then by running it with `java SearchEngine 2850` we add a random 4 digit number at the end of it because that is the port we want to put it in. Then in return we get the output, "Server Started! Visit http://localhost:2850 to visit." which is the link we need to visit for the site.
Below is a picture of what it looks like in the terminal when you run the commands.

![run command for lab 3](https://user-images.githubusercontent.com/66755589/197430006-010beb6f-b1ed-423a-83fb-88237c031b37.png)
 
Here is a picture of what it looks when you put the web site link onto your browser. Since we do not have any "/"s after the first part of the link then the code just goes to the home page. If it did have a "/" then the code would look for the word after it and sort it into different actions based off of that.
![default lab 3](https://user-images.githubusercontent.com/66755589/197433869-51f4a439-e64d-4852-a75f-6ad9180f35f9.png)

Adding Items:


Query:

## Part 2
