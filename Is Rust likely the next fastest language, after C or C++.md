To answer you question: **No, Rust aims at being faster than C.**

Rust programs can be written to be as fast as C programs today already. It's relatively uninteresting though because (1) Rust aims at being both fast and safe, so discarding safety to get speed is annoying, and (2) Rust actually has the potential to be faster than C, and tickle old Fortran.

Whether Rust realizes this potential is a completely different problem, of course. C, C++ and Fortran compilers have decades of optimization under their belt, and the very LLVM optimizer backend that rustc uses is still very much "C" oriented. For example, it has type-based alias analysis (due to C and C++ strict aliasing rules) which is useless in Rust, which has a richer explicit aliasing annotations for its references... which cannot be taken advantage of properly (yet).

There are also issues in other areas, such as optimized integer overflow detection and bounds checking elision, which are not major issues in C or C++ (developers are used to unsafe behavior and reach for it by reflex) but would be very beneficial in Rust to be able to be both safe and yet fast at the same time.

On the other hand, rustc now has MIR (Middle-level Intermediate Language) on which it can apply Rust-centric optimizations before lowering to LLVM IR. It's unclear how much could be done here (without being redundant with LLVM), but there's hope in this direction.

Code written in Rust is and will be faster than C or C++. There are already plenty of examples like:

- https://github.com/BurntSushi/ripgrep

- https://github.com/mmstick/parallel

- https://github.com/jwilm/alacritty

- https://github.com/pcwalton/pathfinder

- https://github.com/ethcore/parity

It's not a coincidence that a lot of Rust projects are the fastest implementation of given thing anywhere, ever.

Code written in Rust is much easier to work with, reuse existing libraries, write tests, refactor, use multi-threading. In real-life project this is going to be the greatest speedup factor.

Plenty of times in C/C++ I ignore small performance waste, just to make the code easier to live with. Especially in C, equipped only with lame macroprocessor I just give up on what could be possible. In C++ it's not much better, since templates combined with all the C++ gotchas, and poorly retrofitted smart-pointers are just barely better.

Simple example: Modern C++ codebases are ridden with shared_ptr which is like Rust's Arc, even if the code is completely single-threaded. Something that in Rust would be done with Rc to avoid atomic instructions, completely safety and refactor-proof. As soon as someone will want to pass such a value to another thread rustc will make sure it's fixed.

C and C++ seeing two pointers, have a hard time telling if they can point to overlapping memory. Lifetimes and ownership and borrowing rules allow much better optimization. Something that in C would require restricted qualifier everywhere, which is done practically never.

Traits and monomorphization make it possible to have very elaborated abstractions that compile to a super-optimized code. C++ can do it, but it's much easier to do in Rust. Throwing a trait here and there is quite easy unlike writing C++ template code.
