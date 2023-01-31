# Week 2 and Week 3 Lab Report

## Part 1

Below is the screenshot of the code used to create StringServer:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.37.12%20PM.png)

The first method is the Handler class which implements URLHandler, modified from the code we worked with during Lab 2. This method looks at the path of a URL and if it contains the "/add-message" part that we are looking for, it will find what string we are passing in to the left of the = sign and adds it to the running string. The method that is called directly is the StringServer main method, which starts the server and will keep it running. The relevant arguments to the first method is the url and paths that are being passed in. The url is then split at the '=' sign to get the relevant string to add to the running string. The value that is being changed each time we pass in a new URL is the running string, and this new string is what will be displayed on the page of the web server. 

Here are two screenshots of what happens after we pass in "/add-message?s=Hello" and then "/add-message?s=How are you":

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.38.23%20PM.png)

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-30%20at%207.38.37%20PM.png)



