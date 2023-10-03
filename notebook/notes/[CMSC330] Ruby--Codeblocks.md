# Ruby: Codeblocks

Created: 2023-01-31 13:59:01 -0500

Modified: 2023-02-09 19:29:22 -0500

---

Making a 2D Array:

- matrix = Array.new(3){ Array.new(3) } = [[nil, nil, nil], [nil, nil, nil], [nil, nil, nil]]
  - Arrays are nil by default, the second parameter allows you to define a default value to fill the array with.
  - { Array.new(3) } is a codeblock

Codeblock

- Other examples:
  - a2d1 = Array.new(3){ Hash.new() } = [{}, {}, {}]
  - a2d2 = Array.new(3){ |i| i } = [0, 1, 2]
- A codeblock is a segment of code that another method uses
  - Enclosed in {} or do ... end
  - |...| marks parameters
  - Codeblocks are **not** objects
  - Main idea: Code treated as data

Proc

- Procs make codeblocks into objects
- They need to be called, not yielded to
  - Ex.
    - def func(p)
      - p.call
    - end
    - p = Proc.new {puts "hello"}
    - func(p)
- Can be strung together
- Codeblocks and Procs are **not** the same
