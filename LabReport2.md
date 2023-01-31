# Week 2 and Week 3 Lab Report

## Part 1

Below is the screenshot of the code used to create StringServer:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.37.12%20PM.png)

The first method is the Handler class which implements URLHandler, modified from the code we worked with during Lab 2. This method looks at the path of a URL and if it contains the "/add-message" part that we are looking for, it will find what string we are passing in to the left of the = sign and adds it to the running string. The method that is called directly is the StringServer main method, which starts the server and will keep it running. The relevant arguments to the first method is the url and paths that are being passed in. The url is then split at the '=' sign to get the relevant string to add to the running string. The value that is being changed each time we pass in a new URL is the running string, and this new string is what will be displayed on the page of the web server. 

Here are two screenshots of what happens after we pass in "/add-message?s=Hello" and then "/add-message?s=How are you":

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.38.23%20PM.png)

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.38.37%20PM.png)

Each time that the url is changed in the search bar, both methods in the code will be called. The main method keeps the server running and the first method does the work of taking in the new path and url and updating the string, which is then displayed once the page is refreshed. The relevant arguments to those methods will be the whole url itself and the relevant field that is changed would be the running string, which has the string to the right of the = sign added to it along with "\n". 

## Part 2

The bug I chose was from the reversed method in ArrayExamples.java, with the JUnit tests in ArrayTests. Here was the code inside the JUnit test that was the failure-inducing input:

`assertArrayEquals(new int[]{6, 5, 4}, ArrayExamples.reversed(new int[]{4, 5, 6}));`

Here was an input that did not produce a failure, as it was testing an empty array:

`assertArrayEquals(new int[]{ }, ArrayExamples.reversed(new int[] {}));`

The symptom we see is that the second JUnit test fails as it saw a different output than what was expected at the first position of the output array:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.56.16%20PM.png)

This was the code used before, which caused the bugs:

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i -1];
    }
    return newArray;
  }
```

The change that needed to be made here was switching the order of `arr` and `newArr` in the line inside the for loop. This code was mistakenly changing the contents of `arr` and returning the new array, when it should be modifying the new array itself. Then, the new array will be keeping track of the elements from the input array in reverse order, and we can return this. 

This is the code after:

```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArr[i] = arr[arr.length - i -1];
    }
    return newArray;
  }
```
## Part 3

From Week 2's lab, I learned how to implement a basic web server. Before, I had seen the localhost url's but didn't know how to interact with them, but in Week 2's lab, I learned how to start the server and use the URLHandler interface to keep track of the changes added to the urls. I also learned how it was not necessary to return to the code or the terminal to do this, as the new string could just be modified in the search bar and browser itself and this change would reflect on the page, whether it was a number being incremented or a string being concantenated. This kind of web server implementation could have several more complex applications, like being used to implement a basic game where parameters are taken in and messages are displayed accordingly. 
