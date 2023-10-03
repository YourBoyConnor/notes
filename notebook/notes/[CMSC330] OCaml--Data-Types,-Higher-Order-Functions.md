# OCaml: Data Types, Higher Order Functions

Created: 2023-02-21 14:04:11 -0500

Modified: 2023-02-28 14:02:05 -0500

---

Data Types:

-   Tuple:
    -   Like a list
        -   Can be heterogeneous (not everything needs to be same type), but fixed size
-   Records:
    -   Like a weird hash
-   Used Defined Types:
    -   Like a typedef
    -   type <keyword> will allow for an alias
    -   Can hold data



Higher Order Functions:

-   Like codeblocks in ruby, but we can do more in Ocaml
-   Anonymous Functions:
    -   A function that is not bound to a variable
        -   Ex. Fun x1 -> x + 3
        -   All functions are anonymous functions with some special syntax
    -   Recall referential transparency:
        -   Functions are expressions, so you can treat them like everything else
            -   Pass in as arguments, have types
-   Map and Fold
    -   Map: Takes in a function and a list, the function is applied to each item in the list, returns new list of output
    -   Fold: Aggregates a list into a single value
    -   Foldr: Same thing, but order of evaluation is reversed


