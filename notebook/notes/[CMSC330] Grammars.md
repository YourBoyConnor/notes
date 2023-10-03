# Grammars

Created: 2023-03-30 14:01:04 -0400

Modified: 2023-03-30 14:19:12 -0400

---

Compiler: convert from language to machine code

- Practically: convert from language to assembly
- Abstracted: convert from language to another

Three things we need for a translator:

- Lexer
  - Typically uses RegEx to convert text to tokens
- Parser
  - Converts tokens to an Abstract Syntax Tree (AST) using a Context Free Grammar (CFG)
- Evaluator/Generator
  - Converts AST to Target

RegEx: Describes a set of strings

CFGs: Describes a set of strings with some stuff that RegEx cannot use

Grammar: Structure of a language

Consider the grammar for /[01]+/:

- S -> 0S|1S|1|0

To generate the string 001:

- S -> 0S
- 0S -> 00S
- 00S -> 001S
- 001S -> 001
- This is called deriving

Recursion allows for repetition

- S -> 0S|ϵ

Separate Non-terminals can be used for concatenation

- S -> AB
- A -> hello
- B -> world

Grammar describes structure of a language, which we can model with a tree

Sometimes multiple trees come out of a single grammar

- Ex.

E→A|E+E|E−E|E∗E|E/E|(E)

A→0|1|...|9|a|b|...|z

- There are left and right derivations

- Sometimes, left derivations have more derivations
  - This is called ambiguity (which is bad)

How to fix ambiguous grammar

- Rewrite the Grammar
  - Ultimately many different ways to describe a set of strings
- Different Parsers have different rules
- Can rewrite above example to:

E→|E+A|E−A|E∗A|E/A

A→0|1|...|9|(E)

- No longer ambiguous, but the problem of precedence still remains
