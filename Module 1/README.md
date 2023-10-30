## Introduction to Garbage Collectors and Object-Oriented Programming 

This lecture will provide a basic understanding of Garbage Collectors (GC) and object-oriented programming (object, references, instantiation) using Pharo. We will present the syntax of the language and explore the Pharo environment. We will some tools to write and execute simple programs.

### Code
- The code of the Swallow class in the `Example.st` file (Example package). Just drag-and-drop the file into the Pharo world and select `Install into the image`.
<img width="661" alt="image" src="https://github.com/PalumboN/garbage-collection-course/assets/4098184/c44e40b4-c0b6-4085-8265-76792759f08d">
- At the end, the code of the _Playground_ was
```st
pepita := Swallow new.
pepita areYouTired.
pepita fly: 50.

Smalltalk garbageCollect.
Smalltalk vm totalGCTime. “2967” “3005”
```

### Links of interest
- Download the Pharo: https://pharo.org/download
- Check the Pharo MOOC: https://mooc.pharo.org/
- Books about Pharo: https://books.pharo.org/

### Practice
- Follow `ProfStef` in the Pharo image to learn how to use the environment.
- Extend the Swallow example (adding tests, adding features, etc).
- Or create a new program (model) that you want.
