# C-Embedded-Questions
The collection of the questions about C/C++ embedded progrramming

## 1. Explain `register` keyword
> It's a hint to the compiler that the variable will be heavily used and that you recommend to keep it in a processor register if possible.
> Registers are in the CPU and much faster to access than RAM. But it's only a suggestion to the compiler, and it may not follow through.

## 2. Explain `restrict` keyword
> It can be used in pointer declarations. It hints to the compiler that for the lifetime of the pointer, no other pointer will be used to access the object to which it points.
> It prevents memory overlapping and optimizes the code(less assembly instructions).
> https://stackoverflow.com/questions/745870/realistic-usage-of-the-c99-restrict-keyword

## 3. Explain `volatile` keyword
> Tells the compiler not to optimize anything that has to do with the volatile variable.
> It is used when the value of the variable can change unexpectedly, such as when it is modified by hardware or by another thread. 
> The compiler is instructed to always re-read the variable's value from memory whenever it is accessed, instead of relying on cached or optimized values

## 4. Explain `extern` keyword
> For variables it doesn't instantiate the variable itself, i.e. doesn't allocate any memory. This needs to be done somewhere else. Thus it's important if you want to import the variable from somewhere else.
> For functions, this only tells the compiler that linkage is extern. As this is the default (you use the keyword static to indicate that a function is not bound using extern linkage) you don't need to use it explicitly.

## 5. Explain `inline` keyword
>  It is used as a hint to the compiler to perform inline expansion of a function.
>  Inline expansion means that the compiler replaces the function call with the actual body of the function wherever the function is called, rather than generating a separate function call.
>  Inlining can improve performance by avoiding the overhead associated with function calls, especially for small, frequently-called functions.

## 6. Explain `__interrupt`, `__irq` keywords
> It is used to declare interrupt service routines (ISRs) . Routine is a function that is executed in response to an interrupt signal from hardware, such as a timer overflow, GPIO pin change, or peripheral event.
> When an interrupt occurs, the processor looks up the corresponding ISR address in the IVT to determine which ISR to execute

## 7. What is `IVT`
> The Interrupt Vector Table is a data structure located in a fixed memory location that holds the addresses of ISR functions corresponding to each interrupt source.
