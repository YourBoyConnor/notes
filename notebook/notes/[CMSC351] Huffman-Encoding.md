# Huffman Encoding

Created: 2023-05-02 11:07:33 -0400

Modified: 2023-05-02 11:51:47 -0400

---

Each character is encoded with 0's and 1's.

-   Problem: It is ambiguous
-   Possible fix:
    -   Use the same number of bits for each character
    -   Use a prefix code (a unique identifier at the beginning of each character)



Huffman encoding encodes a string with 0's and 1's using a Binary Tree.

1.  Build a binary tree based on the frequency of each char
2.  Read the code from the binary tree
3.  Use the code to encode the string



Runtime: O(p) + O(nlogn) + O(p)

It is optimal
