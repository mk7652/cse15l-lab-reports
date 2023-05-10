# Lab Report 3
## `grep` Implementations

`grep` is a command line operation which searches the provided file or files for the provided string and prints the matching lines. Its format is `grep <<string>> <<file>>`. 
Below are some interesting implementations of grep which I found on [wikibooks](https://en.wikibooks.org/wiki/Grep). 

##`grep -i`

`grep -i` searches the provided files for the provided string and ignores case. an example of this command in use is displayed below.

`$ grep -i "all five" technical/911report/chapter-1.txt
 While Atta had been selected by CAPPS in Portland, three members of his hijacking team-Suqami, Wail al Shehri, and Waleed al Shehri-were selected in Boston. Their selection affected only the handling of their checked bags, not their screening at the checkpoint. All five men cleared the checkpoint and made their way to the gate for American 11. Atta, Omari, and Suqami took their seats in business class (seats 8D, 8G, and 10B, respectively). The Shehri brothers had adjacent seats in row 2 (Wail in 2A, Waleed in 2B), in the firstclass cabin. They boarded American 11 between 7:31 and 7:40. The aircraft pushed back from the gate at 7:40.
 All five hijackers passed through the Main Terminal's west security screening checkpoint; United Airlines, which was the responsible air carrier, had contracted out the work to Argenbright Security.`
 
 This command is particularly usefule if you wanted to find a word or words in a document and you dont care if its upper case or lower case. An example of a situation that one might use this in is if you are looking through a document to try to find information about a certian vocabulary term and you dont care if its capital or lowercase because you just want information about the term. It is somewhat similar to `cmd + f` to search through a document for a term.
 
    

