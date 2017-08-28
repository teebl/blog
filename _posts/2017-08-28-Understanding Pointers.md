I have been asked a couple times now by professional programmers if I've started learning pointers yet. They asked the question with a stern look, almost one of concern. My impression is they think I won't make it past it. That I'll throw my hands up in frustration and concede "Computers really ARE hard! I think I'll work in a textile factory instead". They think I'll give up that easy.

It's true, pointers are a challenging part of learning to code. The impression that I get, however, is that these challenges are the bread and butter of tackling this discipline. No heavy lifting, air conditioned offices, and no injuries, save the dent your forehead gets after banging your head against the wall for six hours trying to solve the bug du jour. Frustrating challenges are what makes this stuff 'Work'.

But I get them, the pointers. Obviously that's a bit of a lie, how much can anyone get of anything? I understand the concept, I can navigate the syntax. That's better. For posterity, and maybe a few inquiring minds, here's how I unpacked all of this in my head.

Pointer

A pointer points! It knows where to find a slice of information in a computer. It also knows how big that slice is. In the most literal sense, the pointer is an address (in hexadecimal) of another block in memory.

naming traditions say to throw a 'p' on whatever value is pointing to


##\*\
Dereference Operator

The mysterious asterisk. This one is more challenging because it does more than one thing. In short, it tips off a compiler to use the value pointed to, rather than the address of that value.

Address-of, or, Address-Extraction Operator

This just tells you the address of whatever you pair it with. useful when you need to assign the address to a pointer.







