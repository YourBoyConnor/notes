# 10/5/22 Discussion

Created: 2022-10-05 11:11:31 -0400

Modified: 2022-10-05 11:46:24 -0400

---

Compiler: turns source files (*.c) into object files (*.o)

1.  Source file is preprocessed
2.  Preprocessed file is converted to assembly
3.  Assembler turns assembly into bytecode



Preprocessor symbols:

-   __FILE__: filename, string
-   __LINE__: line, integer
-   __DATE__: date of compilation, string
-   __TIME__: time of compilation, string
-   __STDC__: Whether or not compiler is ANSI-compliant, 1 or undefined

Cannot define the same struct twice

