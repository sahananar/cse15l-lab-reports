# This tutorial will describe how to log onto an account on `ieng6` and run some basic commands

**The first step is to install Visual Studio Code**

To install VScode, first go to this link: [Download VScode](https://code.visualstudio.com/). Follow the instructions to download the application onto your computer and follow the specific download link depending on your operating system. Once you have installed the application, open it up. It should look similar to this:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-12%20at%2010.29.22%20AM.png)

**The next step is to use your course specific account to remotely connect**

First, if you are on windows, you would need to install Git for your device. Once you have Git installed, open a new terminal in VScode. In the terminal, my command looked like this:

`ssh cs15lwi23aqf@ieng6.ucsd.edu`

The letters aqf are unique to my course specific account. If a different username is used, change those 3 letters. When logging in for the first time, a warning message will be displayed asking if you would like to proceed with connecting, to which you should respond with yes. It will then prompt for your password. I had trouble at first logging in with the password I had previously used for my course specific account, so it may be necessary to change your password using the school's website and then wait for up to 15 minutes for the new password to go into effect. Keep in mind that the text will be invisible while you are entering your password, so make sure you didn't mistype. 

Once your password has been accepted, you should see this message pop up at the bottom: 

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-12%20at%2010.37.36%20AM.png)

Now, you are successfully logged in and are remotely connected to a computer in the CSE lab and can run any commands on there from your own device. 

**The final step is try out some of these commands**

These commands can be tried on your own computer, using your built in terminal, or can be run on the remote server, in the VScode terminal after you log in using `ssh`. Here are a few commands to try out:

`pwd` - this will show your location in the current directory
`cd` - this is used to change your directory
`ls - a` - this is used to show hidden files
`ls - lat` - this will display a list of files that are sorted by time
`cat/home/linux/ieng6/cs15lwi23/public/hello.txt` - this uses the filepath of the hello.txt file and the cat command to print the contents of 'hello.txt', which will display the message, 'Hello! Welcome to CSE 15L', as shown in the screenshot below:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-01-12%20at%2011.45.19%20AM.png)

You have now reached the end of this tutorial. You should have been able to successfully use VScode's terminal, remotely connect to the server using your course specific account, and then use this account to run a few important commands using ssh in the terminal. 
