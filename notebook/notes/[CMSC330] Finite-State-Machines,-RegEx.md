# Finite State Machines, RegEx

Created: 2023-03-02 14:00:48 -0500

Modified: 2023-03-02 14:50:15 -0500

---

Quiz tomorrow, everything up to and including Thursday



State Machine: Given a certain input (a state), compute a certain output



Finite State Machines are limited to a specific function, and cannot go outside that

-   Ex. Logic Gates are state machines that are limited to solving logic problems



Combined with an infinite memory stack, this state machine becomes a push-down automata (PDA), which can then be combined with an infinite ticker to create a Turing machine that is created that can solve any solvable problem.



Model of the Universe:

-   ![](../../media/Spring-2023-Organization-of-Programming-Languages-Finite-State-Machines,-RegEx-image1.png)



Regular Expression Definition

-   The alphabet: a set of symbols in a language
    -   Denoted by ∑
    -   String: sequence of symbols from ∑
-   A language: a set of strings
-   Single symbol: a, b, c, &, ^, ...
-   Concatenation: abba, abcd, gk, ...
-   Repetition: aa, bgbg, b, bb, bbb, bbbb, ...
-   Branching/or: a|b, g|j, ...



All of these rules together create a Grammar.



Languages created by Regular Expression are called Regular Languages

-   L is a language created by a RegEx r
-   If a string s is in L, then r must accept s



Finite State Machine examples for Regular Expressions in the Notes (Graph model)

