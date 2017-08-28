  I have been asked a couple times now by professional programmers if I've started learning pointers yet. They asked the question with a stern look, almost one of concern. My impression is they think I won't make it past it. That I'll throw my hands up in frustration and concede "Computers really ARE hard! I think I'll work in a textile factory instead". They think I'll give up that easy.

It's true, pointers are a challenging part of learning to code. The impression that I get, however, is that these challenges are the bread and butter of tackling this discipline. No heavy lifting, air conditioned offices, and no injuries, save the dent your forehead gets after banging your head against the wall for six hours trying to solve the bug du jour. Frustrating challenges are what computers are really made of.

But I get them, the pointers. Obviously that's a bit of a lie, how much can anyone get of anything? I understand the concept, I can navigate the syntax. That's more accurate. For posterity, and maybe a few inquiring minds, here's how I unpacked all of this in my head.

## Pointer

A pointer points! It knows where to find a chunk of information in a computer. It also knows how big that slice is. In the most literal sense, the pointer is an address (in hexadecimal) of another block in memory.

How is this useful? It allows two functions to share the same bit of data. This is like two people sharing a notepad, rather than each having to keep a copy. They can use updated info immediately.

*eg: pname*

*Naming traditions say to throw a 'p' on whatever value the pointer is pointing to*


## \* (Dereference Operator)

The mysterious asterisk. This one is more challenging because it does more than one thing. In short, it tips off a compiler to use the value pointed to, rather than the address of that value.

*eg \*px*

*eg:int\**

*This indicates the value declared is a pointer, specifically for an int-sized block of memory*

## & (Address-of Operator)

This just tells you the address of whatever you pair it with. useful when you need to assign the address to a pointer.

*eg: &name_string*


---

Here's a bit of a demonstration:

```c
// first, declare a simple variable

int x = 0;

// Here, I'll make px a pointer, with the address of x the place it's pointing to

int* px = &x;

// Here, px equals something like 0xe34f44ea, the address of x

// I want to change the value of x, and I can do so by using px. I just need a dereferencing operator

*px = 1

//now, if I were to ask the value of x, I'd get a 1 back

```

---
The jist of what I know is this: A pointer is useful for sharing a block of data between multiple functions. This means you can change a word to pig latin in one function, and then the happy birthday function that declared the name variable will be just that much sillier. It's important to remember when you're manipulating a value, and when you're manipulating the address the pointer is holding onto. The dereferencing operator is important in this.


There is certainly more to pointers, just like everything else in programming, but I think this is enough to wet your palate. Have a great week!






