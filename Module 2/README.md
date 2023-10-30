## Introduction to Garbage Collector

### Lecture
- Introduction to Garbage Collectors (GC) in the context of object-oriented programs. 
- We will describe how the GC is implemented inside the Pharo Virtual Machine.

### Testing
First, we can check/create some tests in the VM code:
- Create a graph of objects and run the GC
- Validate died/alive objects

### Practice
Then, we can run some programs created on the previous lecture:
- Are them "memory-starved" applications? (Check the GC overhead!)
  - `If yes` -> How do you know? Any idea about where could be the issue?
  - `else`  -> Make sense with the program behaviour? Can you modify it to increase the memory usage?
