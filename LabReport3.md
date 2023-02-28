# Lab Report 3 - Researching Commands

## Example 1:

The `grep -r` command, which you can use to get all of the filenames in a directory which contain a certain string as well as the lines in each file containg that specific string. For these examples, I was in the skill-demo1-data directory and written_2 was inside. 

Input 1:
```
grep -r "Italy" written_2
```
Output 1 (there were several more lines that were outputted, this screenshot shows the first few filenames)

```
written_2/non-fiction/OUP/Castro/chP.txt:The word piñata derives from the verb apiñar, which means to 
cram, tie, or join together. In Italy pignattas were hung from the ceilings during masquerade balls. 
It is accepted that there is an oriental influence, since piñatas are always decorated with colorful 
crepe paper. It is thought piñatas originated in China and were brought to 
Sicily and Spain by the Arabs and to New Spain by the Spaniards.
```

Input 2:
```
grep -r "magnificent" written_2/travel_guides
```
Output 2 (there were several more lines that were outputted, this screenshot shows the first few filenames)

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-02-13%20at%208.08.39%20PM.png)

Sources used: I asked Chat GPT for how to search for a specific string among multiple files in a directory. 

## Example 2:

The `grep -A <N>` and `grep -C <N>` commands. For the first example, I used 'grep -A <N>', which will print the line in the file which contains the given string, along with N lines that follow the match. For the second example, I used 'grep -C <N>', which will show the matching line as well as N number of lines surrounding the matching line. 

Input 1:
```
grep -A 1 "Italy" written_2/travel_guides/berlitz1/WhatToItaly.txt
```
Output 1:

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-02-13%20at%208.36.38%20PM.png)

Input 2:
```
grep -C 2 "Italy" written_2/travel_guides/berlitz1/WhatToItaly.txt
```
Output 2: 

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-02-13%20at%208.36.57%20PM.png)

Sources used: I found [this link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/) through a web search about different grep commands. 
  
## Example 3:
  
The `grep -c` command. If you use this command along with a string and a filename, it will count how many matches of that string there are within the file. 

Input 1:
```
grep -c "beach" written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
```
Output 1:
`17`

Input 2:
```
grep -c "island" written_2/travel_guides/berlitz1/IntroGreek.txt
```
Output 2: 
`22`

Sources used: I found [this link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/) through a web search about different grep commands. 
  
## Example 4:
  
The `grep -v -c` command, which is the opposite of the command used in example 3. If you use this command along with a string and a filename, it will count how many lines in the file do not contain that specific string. 

Input 1:
```
grep -c "beach" written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
```
Output 1:
`108`

Input 2:
```
grep -c "island" written_2/travel_guides/berlitz1/IntroGreek.txt
```
Output 2: 
`104`

Sources used: I found [this link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/) through a web search about different grep commands. 
