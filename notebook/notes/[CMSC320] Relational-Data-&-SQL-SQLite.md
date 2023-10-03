# Relational Data & SQL/SQLite

Created: 2023-02-16 15:32:39 -0500

Modified: 2023-02-16 16:01:45 -0500

---

Simplest relation: a table full of unique tuples

Primary keys: ID above, every tuple has exactly 1 primary key

Foreign keys: Attributes that point to a different table's primary key, can have multiple

Searching: By keeping a sorted list of attributes, you can use binary search instead of sequential so that it is O(logn), not O(n)

Primary keys and Foreign keys define interactions between different tables/entities:

- One-to-one
- One-to-one-or-none
- One-to-many and many-to-one
- Many-to-many

Ex. One to Many:

- One nationality can connect to many people

Ex. One-to-One:

- Each person has one Social Security number

Ex. One-to-One or None:

- A person can have 1 or 0 cats

Ex. Many-to-Many

- Tracking the coloring of cats, each cat can have many colors, each color can have multiple cats

Will be using sqlite3, crash course on connecting to/creating a database:

SQL Rules/Tips for class:

- Caps don't matter, but capitalize keywords for readability
- Cursor.execute to push SQL operations
- Can read a SQL database into a pandas dataframe
- Joining:
  - Inner
    - Returns merged rows that share the same values that you are comparing.
  - Left
    - Get all results that appear in the left table, and only results that match in the right side
  - Right
    - Opposite of left
  - Full Outer
    - Combine left and right tables, and fill in information that doesn't match with NULL

You can use raw SQL in pandas with pandasql (pip install pandasql) with """
