# Lab Report 3 - Researching Commands

## Example 1:

The `grep -r` command, which you can use to get all of the filenames in a directory which contain a certain string as well as the lines in each file containg that specific string. For these examples, I was in the skill-demo1-data directory and written_2 was inside. 

Input 1:
```
grep -r "Italy" written_2
```
Output 1 - There were several more lines that were outputted, this code block shows just the first results. The lines were intentionally spaced this way so that the code block would not get cut off. 

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
Output 2 -

```
written_2/travel_guides/berlitz1/HandRMadrid.txt: near the Royal Palace, occupies a magnificent palace and converted
written_2/travel_guides/berlitz1/HistoryEgypt.txt: history of Egypt ruled for over 60 years and supervised magnificent
written_2/travel_guides/berlitz1/HistoryEgypt.txt: magnificent Abu Simbel. Some scholars now postulate that Ramses II was
written_2/travel_guides/berlitz1/HistoryGreek.txt: settlements of Thira and Akrotiri thrived at this time. The magnificent
written_2/travel_guides/berlitz1/HistoryIndia.txt: east–west trade and so were able to finance the magnificently sculpted
...
```

Sources used: I asked Chat GPT for how to search for a specific string among multiple files in a directory. 

## Example 2:

The `grep -A <N>` and `grep -C <N>` commands. For the first example, I used 'grep -A <N>', which will print the line in the file which contains the given string, along with N lines that follow the match. For the second example, I used 'grep -C <N>', which will show the matching line as well as N number of lines surrounding the matching line. 

Input 1:
```
grep -A 1 "Italy" written_2/travel_guides/berlitz1/WhatToItaly.txt
```
Output 1:

```
day when Italy is involved in a major international football match,
        streets all over the country are deserted — until the cars come out

round-Italy Giro d’Italia in June. You can watch world championship
        skiing at Cortina d’Ampezzo and Val Gardena. Bocce, the bowling game

Motor racing fans can watch the Grand Prix of Italy at
        Monza, near Milan, or at Imola, near Bologna.

clothing. You can rent horses for riding throughout Italy — Tuscany and
        Umbria provide especially scenic terrain.
```

Input 2:
```
grep -C 2 "Italy" written_2/travel_guides/berlitz1/WhatToItaly.txt
```
Output 2: 

```
  Witness the crowd’s unashamedly chauvinistic partisanship at
        Rome’s international open tennis championships or the Davis Cup. On a
        day when Italy is involved in a major international football match,
        streets all over the country are deserted — until the cars come out
        honking for a frenetic victory parade or the men shuffle on foot to the
--
        Naples.
        Cycling races are still popular — especially the
        round-Italy Giro d’Italia in June. You can watch world championship
        skiing at Cortina d’Ampezzo and Val Gardena. Bocce, the bowling game
        similar to French boules or pétanque, is played in small towns wherever
        there’s a patch of tree-shaded sand or gravel and a bar close enough at
        hand to serve a glass of wine or grappa.
        Motor racing fans can watch the Grand Prix of Italy at
        Monza, near Milan, or at Imola, near Bologna.
        On the beaches of the Adriatic coast, the Italian Riviera,
```

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
