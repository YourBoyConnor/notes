# 10/10/22 Discussion

Created: 2022-10-10 11:12:10 -0400

Modified: 2022-10-10 11:49:31 -0400

---

Gcc -c hashtable.c -> Would compile hashtable.o



Makefiles:



Ex.

publicX.o: publicX.o puzzles.o

gcc -o publicX publicX.o puzzles.o

publicX.o = target

publicX.o puzzles.o = dependencies

Gcc -o publicX publicX.o puzzles.o = commands



Need to create object files in the makefile as well!

publicX.o: publicX.c puzzles.h

gcc -c publicX.c

-MM options displays the dependency for a .c file




