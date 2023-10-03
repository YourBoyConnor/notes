# OCaml: Intro to Functional Languages

Created: 2023-02-14 14:00:12 -0500

Modified: 2023-02-14 15:26:36 -0500

---

Functional Programming: a programming paradigm (way of defining and solving problems) based on functions

Programming Paradigm: classification of programming approach based behavior of code

- Typically used interchangeably with language features
- Ruby is imperative, object-oriented, reflective and technically functional, while OCaml is only imperative, object-oriented and functional

Features of functional languages

- Immutable State
- Declarative Programming
- Referential Transparency
- Realistic about the Machine

Program State: the state of the machine at any given time, usually contents of variables

Imperative: State is mutable, changing, or destructive

- This can cause unintended side effects in programs (Bad)
- Functional Programming prevents this with an immutable state
  - Minimizes side effects
  - Assumes referential transparency
  - Builds correct programs

(Lack of) Referential Transparency: replacing an expression with value with no side effects

If is an expression, functions are expressions

Type Inference: inferring a variable's type

Types are inferred by options they use:

1. (*types.ml*)
2. (*compare two same types*)
3. 1 = 1
4. x = y
5. x > y
6. x < y
7. (*x and y must have the same type*)
8.  
9. (*int have operators*)
10. 3 + 4
11. x - y
12. x * y
13. x / y
14. x mod y
15.
16. (*floats have different ones*)
17. 3.2 +. 4.
18. x -. y
19. x *. y
20. x /. y
21.
22. (*Strings have some too*)
23. "hello" ^ " world"
24.
25. (*latent typing means inference*)
26. let f x y = if x > y then x else y-4;;
27. (*int -> int -> int*)
