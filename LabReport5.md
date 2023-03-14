# Lab Report 5

The lab activity I chose to investigate further was the one about `find` and `grep` commands. 

Below, I have included a few examples using new commands we did not cover in class on the files from the written_2 folder, and code blocks of their outputs. 

## Example 1:

The `grep -r` command, which you can use to get all of the filenames in a directory which contain a certain string as well as the lines in each file containg that specific string. For these examples, I was in the skill-demo1-data directory and written_2 was inside. 

Input:
```
grep -r "Italy" written_2
```
Output:

```
written_2/non-fiction/OUP/Castro/chP.txt:The word piñata derives from the verb apiñar, which means to 
cram, tie, or join together. In Italy pignattas were hung from the ceilings during masquerade balls. 
It is accepted that there is an oriental influence, since piñatas are always decorated with colorful 
crepe paper. It is thought piñatas originated in China and were brought to 
Sicily and Spain by the Arabs and to New Spain by the Spaniards.
```

## Example 2:
  
The `grep -c` command. If you use this command along with a string and a filename, it will count how many matches of that string there are within the file. 

Input:
```
grep -c "beach" written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
```
Output:
`17`
  
## Example 3:
  
The `grep -v -c` command, which is the opposite of the command used in example 3. If you use this command along with a string and a filename, it will count how many lines in the file do not contain that specific string. 

Input:
```
grep -c "beach" written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt
```
Output:
`108`
