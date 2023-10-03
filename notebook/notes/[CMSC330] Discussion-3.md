# Discussion 3

Created: 2023-02-10 14:02:44 -0500

Modified: 2023-02-10 14:12:01 -0500

---

Steps for what Data Structure to use:

1.  Outline the problem
2.  What would make it easier to solve this problem?



generatePOS(sentence)

1.  Split up the sentence into words
2.  Find what POS each word is

-   Issues we could run into while coming up with a solution:

    a.  Words can have multiple POS

    b.  IF the word is in another language (not english) the POS is harder to find



generatePOS("der blau lkw") -> "the blue truck" in German

DET



Data Structure:

@@words -> {}



Key -> English word

Value -> ???



Assuming that the sentence is in the right grammar:

1.  Find the language of the sentence
2.  Return language's grammar



Assuming that the sentence is not always the right grammar BUT all words only have 1 POS:

1.  Data structure = Hash {key -> english word, value -> POS}



What if same word in different language with a different POS



Data Structure:

-   Each language has its own hashmap
-   "english" -> Object?
