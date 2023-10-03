# Ruby: Regular Expressions (RegEx)

Created: 2023-02-07 13:57:37 -0500

Modified: 2023-02-07 15:08:00 -0500

---

For the most part, everything on a UNIX system is a file

-   Programs live in RAM
-   Files live in LTS (long-term storage)
-   Programs read files to pick up where they left off
    -   Saves, Configurations, etc.
-   To read files in Ruby, there are methods that can be accessed by the File class.
    -   f = File.open
    -   f.gets # single line
    -   f.readlines # reads all the lines into memory



Interesting String Interactions and Methods

-   a = "hellon"

Remove Ending Values

-   a.chomp # returns "hello" with no newline, but does **not** modify a
-   a.chomp! # returns the same, but removes the newline from a

Substrings

-   Puts a[1] = "e"
-   Puts a[-1] = "o"
-   Puts a[1..] = "ello" # inclusive substring (can also put an ending bound)
-   Puts a[1...3] = "el" # exclusive substring

Substitution

-   a = "hello world"
-   a["world"] = "cliff"
-   Puts a = "hello cliff" # can index with a substring
-   a.sub!("hello", "bye") # will sub first instance of the substring
-   a.gsub(...) # will sub all instances of the substring

Searching

-   a = "hello world"
-   Puts a.include?("hello") # returns a boolean of whether the argument is found within the string
-   Puts a.index("o") # returns the index of the found argument within the string



Regular Expression: A pattern that describes a set of strings

-   Regular Expressions are used to describe regular languages
-   For now: a tool used to search for text

What is RegEx useful for searching?:

-   A pattern that describes a set of strings
    -   Alphabet
    -   Concatenation
    -   Branching (or)
    -   Grouping
    -   Repetition
-   =~: RegEx matching operator
-   Regex Examples:
    -   Line =~ /cliff|kliff/ # contains cliff or kliff
    -   Line =~ /(c|k)liff/ # contains cliff or kliff
    -   Line =~ /[a-z]liff/ # includes 'liff'
    -   Line =~ /[a-z]{5}/ # any 5 letter string
    -   Line =~ /[0-9]{1, 3} # any 1, 2, or 3 digit number
    -   Line =~ /-?[0-9]+/ # any integer
    -   Line =~ /-?[0-9]+(,-?[0-9]+)*/ # a list of numbers
    -   Line =~ /^start d* end$/ # start number end
    -   Line =~ /[^start]$d+.d{2}/ # start number end



Useful Ruby RegEx editor: [www.rubular.com](http://www.rubular.com)