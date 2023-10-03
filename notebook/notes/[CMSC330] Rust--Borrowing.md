# Rust: Borrowing

Created: 2023-05-02 12:38:10 -0400

Modified: 2023-05-02 13:42:42 -0400

---

Using the & operator, you can allow a function to use a value that is owned by another variable without making the original variable lose ownership (called borrowing)



Ex.



fn main() {

let x = String::from("Hello");

let y = get_len(&x)

}



fn get_len(x: &string) -> u32 {

x.len()

}



Rules of borrowing:

1.  EITHER a 0R b, NOT BOTH

    a.  One mutable borrow at a time

    b.  Any number of immutable borrows at a time

2.  All references must be valid



Ex.



fn main() {

let mut x = String::from("Hello");

// Both x and &x are now immutable since only one mutable borrow can exist

y = &x

}



Each variable has a lifetime that extends from when it is defined to when it either goes out of scope or is last used



Scope and variable lifetime are not interchangeable in Rust

A variable can be in scope but have a shorter lifetime, see below:



1 Fn main() {

2 let mut s = String::from("Hello");

let r1 = &s;

let r2 = &s;

println!("{} = {}", r1, r2);



let r3 = &mut s;

println!("{}", r3)

println!("{}", r1) // fails

}



At line 9, r1 has an existing mutable and immutable reference, which breaks the code



Lifetime of owner must be >= lifetime of a reference/borrowed reference to the owner to avoid dangling pointers



I need to switch to markdown in VS Code, the code formatting options in OneNote suck ass



More goofy lifetime vs. scope examples from class



'a -> lifetime indicator, will tell compiler that all of these variable need to at least live as long as each other



fn longest<'a> (a: &'a string, b: &'a string) -> 'a string {

...

}



Rust Lifetime Rules:

1.  Compiler will assign a lifetime parameter to each parameter that is a reference
2.  If there is exactly one lifetime parameter, that lifetime is assigned to all output references
3.  If there are multiple input parameter and one of the reference is self or &self, then the output lifetime becomes the same as self or &self.



Rust Custom Data Types:

-   Structs: similar to C structs or objects
-   Enums: similar to OCaml types
-   Traits: similar to Java interfaces



Ex.



struct Rect {

width: u32

height: u32

}



impl Rect {

fn area (&self) -> u32 {

Self.width * self.height

}



fn newf(&self, a: &u32) {

...

}

}



let r1 = Rect{width = 5; height = 10;};

r1.area();

R1.newf(5)


