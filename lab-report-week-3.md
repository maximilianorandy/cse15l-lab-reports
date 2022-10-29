Week 3 Lab

[Week 3 ](https://ucsd-cse15l-f22.github.io/week/week3/#week3-lab-report)

# Part 1

## Code

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

## Default:

So to even start the website, to get to the default page you need to run the code first by compling it in the terminal with the command `javac Server.java SearchEngine.java` and then by running it with `java SearchEngine 2850` we add a random 4 digit number at the end of it because that is the port we want to put it in. Then in return we get the output, `Server Started! Visit http://localhost:2850 to visit.` which is the link we need to visit for the site.
Below is a picture of what it looks like in the terminal when you run the commands.

![run command for lab 3](https://user-images.githubusercontent.com/66755589/197430006-010beb6f-b1ed-423a-83fb-88237c031b37.png)
 
Here is a picture of what it looks when you put the web site link onto your browser. Since we do not have any "/"s after the first part of the link then the code just goes to the home page. If it did have a "/" then the code would look for the word after it and sort it into different actions based off of that. The part that takes us just to the website is called the "domain". The link for the image below we used here is `http://localhost:2850` the domain is infront of the path then goes the query.

![default lab 3](https://user-images.githubusercontent.com/66755589/197433869-51f4a439-e64d-4852-a75f-6ad9180f35f9.png)

## Adding Items:

Here we added items arraylist that holds the information of the website. The code knows that we where trying to add an item because of the `/add` in the URL that is called the path and that is where it tells us what action we are going to be doing the `/` tells the code that its starting to go down a path. The the part after it is `?` which signifies that we are now in the query part of the URL. After that there is `s` which signifies the start of the items we are adding to the storage. Finally comes `=` which seperates the URL pieces from what we are going to add. Whatever we write gets added to the arraylist and its what you can see in the screen shot below. The link for the first example we used here is `http://localhost:2888/add?s=pineapple` the domain is infront of the path then goes the query. We added pineapple, apple, and anewstringtoadd to the arraylist.

![pineapple added](https://user-images.githubusercontent.com/66755589/197440102-1ad3e478-7090-40bf-9e95-6162b14617ce.png)

![apple added](https://user-images.githubusercontent.com/66755589/197440107-26397848-3bdd-4392-bfea-21143880d087.png)

![add a new string lab 3 picture](https://user-images.githubusercontent.com/66755589/197440113-43337b58-efcb-4799-927f-f3da0cd2cfb0.png)

## Query:

To search through the data base we have to have the path set to `/search` which will put you through the if statement on the code. Then like before the question mark `?` is used to help signify that you are in the query part of the URL. Then you will continue with the rest like before, so you add `s` and `=` to tell it your going to start to say what you want to find. Lastly is where we put what we are looking for so in the example below we put that we are looking for 'app' we are looking for anything that contains that sequence of characters in a row within the list. So in the end the link would be `http://localhost:2888/search?s=app` that is what I used to access the page below.

![search function](https://user-images.githubusercontent.com/66755589/197440250-0c97e6b2-1586-4b6d-b913-2639b66ed9cd.png)

# Part 2

## Bug 1:

## Bug 2: reverseInPlace() Method

The reverseInPlace method is supposed to reverse the order of all the items in the input method.

**Original Code**
'''
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
'''

**The failure-inducing input:**

For the test we input an array with {1,2,3,4} and we expected to get it back with the order reversed so it would look like this {4,3,2,1}...

```
@Test 
	public void testReverseInPlace() {
    int[] input = {1,2,3,4};
    int[] expected = {4,3,2,1};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(expected, input);
	}
```
**Symptom:**  The output information that we got from the junit test was "arrays first differed at element [2]; expected:<2> but was:<3>"

**Bug:**  After looking at the code I noticed that the code was taking half of the code and mirroring it to the other side. I noticed this because the array was {4,3,3,4} after we would put it through the method. It was doing this because of how there was no temporary spot to hold the item from one spot so it could be placed in another, the code was putting the item from the opposite index into the spot that the for loop was going through without putting the spot we where looking at to another place. This cause for only half of the array to be coppied to the other side. The way I fixed the bug was by dividing the loop by 2 this made it would it would only cycle through half the list. Then I made a tempary varriable and that varriable would hold the item we where looking at then the item we put into the temporary spot would get the item held in the opposite idex on the array. Then I set the item from the opposite side to the temporary value and it would do this and cycle thriough half the list so it would only hit half of the items and switch them all.

**Revised Code:**
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i]
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i -1] = temp;
    }
  }
```
**Conection:** The




