Week 3 Lab

[Week 3 ](https://ucsd-cse15l-f22.github.io/week/week3/#week3-lab-report)

## Part 1

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

## Part 2
