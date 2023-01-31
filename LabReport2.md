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

A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
