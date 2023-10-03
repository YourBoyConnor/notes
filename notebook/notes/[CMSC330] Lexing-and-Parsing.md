# Lexing and Parsing

Created: 2023-03-30 14:01:25 -0400

Modified: 2023-03-30 14:34:43 -0400

---

Lexing(Tokenizing): Converting a string to a list of tokens

Token: A meaningful string

-   Typically: keywords, identifiers, numbers
-   "The short Wizard" ⇒ [Det;Adj;noun]



How to Tokenize:

-   RegEx and boring repetition
-   Parsing: Taken list to AST
    -   Can check if text is grammatically correct
    -   Many types of parsers: we will use recursive decent
    -   Recursive Decent Parsing (RDP) is top down; Grammar slides showed bottom up



Consider the basic grammar for polish notation: E→A|+A E|−A E

A→0|1|...|9

-   Which branch/token am I in/looking for?
    -   Backtracking vs. Predictive
        -   Predictive: What's the next symbol?
        -   First(nt): set of terminals nt represents



Converting to AST

-   Modify the OCaml tree for tokens
