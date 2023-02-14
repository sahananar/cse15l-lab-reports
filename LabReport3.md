# Lab Report 3 - Researching Commands

## Example 1:

The `grep -r` command, which you can use to get all of the filenames in a directory which contain a certain string as well as the lines in each file containg that specific string. For these examples, I was in the skill-demo1-data directory and written_2 was inside. 

Input 1:
```
grep -r "Italy" written_2
```
Output 1 (there were several more lines that were outputted, this screenshot shows the first few filenames)

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-02-13%20at%208.03.16%20PM.png)

Input 2:
```
grep -r "magnificent" written_2/travel_guides
```
Output 2 (there were several more lines that were outputted, this screenshot shows the first few filenames)

![Image](https://raw.githubusercontent.com/sahananar/cse15l-lab-reports/main/Screen%20Shot%202023-02-13%20at%208.08.39%20PM.png)

Sources used: I asked Chat GPT for how to search for a specific string among multiple files in a directory. 

## Example 2:

The `grep -A <N>` and `grep -C <N>` commands. For the first example, I used 'grep -A', which 

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

Sources used: I this [Link](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/) through a web search about different grep commands. 

