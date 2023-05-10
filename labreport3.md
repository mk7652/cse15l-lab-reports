# Lab Report 3
## `grep` Implementations

`grep` is a command line operation which searches the provided file or files for the provided string and prints the matching lines. Its format is `grep <<string>> <<file>>`. 
Below are some interesting implementations of grep which I found on [wikibooks](https://en.wikibooks.org/wiki/Grep). 

##`grep -i`

`grep -i` searches the provided files for the provided string and ignores case. an example of this command in use is displayed below.

`Mias-Air:stringsearch-data  miakhattar$ grep -i "all five" technical/911report/chapter-1.txt
 While Atta had been selected by CAPPS in Portland, three members of his hijacking team-Suqami, Wail al Shehri, and Waleed al Shehri-were selected in Boston. Their selection affected only the handling of their checked bags, not their screening at the checkpoint. All five men cleared the checkpoint and made their way to the gate for American 11. Atta, Omari, and Suqami took their seats in business class (seats 8D, 8G, and 10B, respectively). The Shehri brothers had adjacent seats in row 2 (Wail in 2A, Waleed in 2B), in the firstclass cabin. They boarded American 11 between 7:31 and 7:40. The aircraft pushed back from the gate at 7:40.
 All five hijackers passed through the Main Terminal's west security screening checkpoint; United Airlines, which was the responsible air carrier, had contracted out the work to Argenbright Security.`
 
 This command is particularly usefule if you wanted to find a word or words in a document and you dont care if its upper case or lower case. An example of a situation that one might use this in is if you are looking through a document to try to find information about a certian vocabulary term and you dont care if its capital or lowercase because you just want information about the term. It is somewhat similar to `ctrl + f` to search through a document for a term. Another example of it being used is seen below. 
 
 `Mias-Air:stringsearch-data  miakhattar$ grep -i "eleven" technical/911report/chapter-1.txt
    The hijackers attacked at 9:28. While traveling 35,000 feet above eastern Ohio, United 93 suddenly dropped 700 feet. Eleven seconds into the descent, the FAA's air traffic control center in Cleveland received the first of two radio transmissions from the aircraft. During the first broadcast, the captain or first officer could be heard declaring "Mayday" amid the sounds of a physical struggle in the cockpit. The second radio transmission, 35 seconds later, indicated that the fight was continuing. The captain or first officer could be heard shouting:" Hey get out of here-get out of here-get out of here."
    The NEADS technician who took this call from the FAA immediately passed the word to the mission crew commander, who reported to the NEADS battle commander: Mission Crew Commander, NEADS: Okay, uh, American Airlines is still airborne. Eleven, the first guy, he's heading towards Washington. Okay? I think we need to scramble Langley right now. And I'm gonna take the fighters from Otis, try to chase this guy down if I can find him.`
 
 ##`grep -o`
 
`grep -o` searches the given file for the specified string and just prints out the string in the line of the file. An example of this is seen below.
 
 `Mias-Air:stringsearch-data  miakhattar$ grep -o "contract" technical/911report/chapter-1.txt
 contract
 contract
 contract
 contract`

This command seems to only be useful if you want to see how many times the exact string appears in the given file. I noticed that even though the string `"contracted"` appears in the file it only prints out the string `"contract"`. If the string doesn't exist in the file then nothing is printed as seen below.

`Mias-Air:stringsearch-data  miakhattar$ grep -o "duck" technical/911report/chapter-1.txt`

##`grep -l` 

`grep -l` searches the given files for the specified string and prints out the matching file which contains the string only. An example of this is seen below.

`Mias-Air:stringsearch-data  miakhattar$ grep -l "contract" technical/911report/chapter-1.txt
technical/911report/chapter-1.txt
Mias-Air:stringsearch-data  miakhattar$ grep -l "contract" technical/911report/chapter-2.txt`

I noticed that when I used `grep -l` on a file which contained the string then it printed out the file, but if I used it on a file which did not contain the string it would print out nothing as displayed by `$ grep -l "contract" technical/911report/chapter-2.txt`. This might be useful if you wanted to see which file contains the string you want to look for before actually searching for the string itself in the file. You could also probably combine this with `grep -i` to search for both upper and lower case at the same time as displyed by the commands and outputs below. 

`Mias-Air:stringsearch-data  miakhattar$ grep -l -i "all five" technical/911report/chapter-1.txt
technical/911report/chapter-1.txt
Mias-Air:stringsearch-data  miakhattar$ grep -l "all five" technical/911report/chapter-1.txt`

##`grep -n` 

The last `grep` command i will be talking about is `grep -n`. This command takes in a string and searches a given file for it and prints out the lines and the line numbers as well. An example of this may be seen below.

`Mias-Air:stringsearch-data  miakhattar$ grep -n "All five" technical/911report/chapter-1.txt
34:    While Atta had been selected by CAPPS in Portland, three members of his hijacking team-Suqami, Wail al Shehri, and Waleed al Shehri-were selected in Boston. Their selection affected only the handling of their checked bags, not their screening at the checkpoint. All five men cleared the checkpoint and made their way to the gate for American 11. Atta, Omari, and Suqami took their seats in business class (seats 8D, 8G, and 10B, respectively). The Shehri brothers had adjacent seats in row 2 (Wail in 2A, Waleed in 2B), in the firstclass cabin. They boarded American 11 between 7:31 and 7:40. The aircraft pushed back from the gate at 7:40.
42:    All five hijackers passed through the Main Terminal's west security screening checkpoint; United Airlines, which was the responsible air carrier, had contracted out the work to Argenbright Security.`

This would allow the person searching for a specific string to see what line it is on to go to that line and read around it for more context. This would especially be helpful in larger files with lots of strings. Below it is also seen working with `grep -i` to search for the string regardless of case. I can be sure they are both working as when I searched for `"all five"` nothing came up.

`Mias-Air:stringsearch-data  miakhattar$ grep -n -i "all five" technical/911report/chapter-1.txt
34:    While Atta had been selected by CAPPS in Portland, three members of his hijacking team-Suqami, Wail al Shehri, and Waleed al Shehri-were selected in Boston. Their selection affected only the handling of their checked bags, not their screening at the checkpoint. All five men cleared the checkpoint and made their way to the gate for American 11. Atta, Omari, and Suqami took their seats in business class (seats 8D, 8G, and 10B, respectively). The Shehri brothers had adjacent seats in row 2 (Wail in 2A, Waleed in 2B), in the firstclass cabin. They boarded American 11 between 7:31 and 7:40. The aircraft pushed back from the gate at 7:40.
42:    All five hijackers passed through the Main Terminal's west security screening checkpoint; United Airlines, which was the responsible air carrier, had contracted out the work to Argenbright Security.`
