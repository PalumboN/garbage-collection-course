# Understanding Garbage Collectors in Object-Oriented Programming (application's allocation patterns study)

Course about Garbage Collection using the Pharo for CERCIRAS - dicated at Riga '23.

## Outline

Automatic memory management is often supported by Garbage Collectors (GC). A GC deals with different programs that manipulate different data. This data must be allocated in the memory (heap), accessible when the application uses it and will be freed when is not necessary anymore (allocation pattern). GCs try to predict the allocation pattern of running applications for better performance. So, they implement parametric algorithms to adapt their complex behaviour to each specific application. There are reports about how garbage collection impacts application performance if not tuned properly, but most developers do not know how the GC works with their programs.
In this lecture series, we introduce how Garbage Collectors work in the context of object-oriented programs. We use the Pharo language to profile the program allocations and analyse profile data. We will analyse applications with different allocation patterns and identify possible causes of performance degradation (pathological cases). We use this information for tuning GC parameters and improving the application’s performance.

## Material

You can 
- **clone** this repository if you know git
- or **download** all the material by [clicking here](https://www.dropbox.com/scl/fi/u9lxkmgmyl10vtpjaqzm8/garbage-collection-course.zip?rlkey=tj6mz27h03taau9m44iiuezm7&dl=0) (don't use the GitHub option to download the `.zip`, videos could be corrupted).

This course is self-contained. All the material to follow the course is here, except the links.
You will only need internet during the software instalation at the beggining of the course and for the last experience.

## Structure

This course is divided into four modules. You will see a folder for each of them + a folder with “VMs for GC profiling” that contains the material for the practical part of the course.

For each module, you will find:
- A _video-lecture_ explaining the module’s topic and showing practical examples.
- The _slides_ used in the video.
- Some _code_ used in the video.
- A `README.md` file with _instructions_ about the activity and related links.


## Modules

- **[Module 1](/Module%201): Introduction to Garbage Collectors and Object-Oriented Programming**
This lecture will provide a basic understanding of Garbage Collectors (GC) and object-oriented programming (object, references, instantiation) using Pharo. We will present the syntax of the language and explore the Pharo environment. We will some tools to write and execute simple programs.
- **[Module 2](/Module%202): Generational Garbage Collector**
The lecture will introduce High-Performance Garbage Collectors, particulary the Generational Garbage Collector algorithm. We will describe how the GC is implemented inside the Pharo Virtual Machine and create some programs to stress the GC in different ways.
- **[Module 3](/Module%203): Analysis of application’s allocation patterns**
We will profile the Garbage Collector events for different application executions. We will analyse profile data based on different charts for understanding how the GC interacts with running applications.
- **[Module 4](/Module%204): Tuning the Garbage Collector**
We will present a pathological allocation case study. We will use the knowledge and tools from previous lectures to identify the possible causes of performance degradation. We will tune the GC to achieve a better application performance.

## Bibliography
1. L. P. Deutsch, D. G. Bobrow, An efficient, incremental garbage collector, CACM 19 (1976) 522–526.
1. D. Ungar, Generation scavenging: A non-disruptive high performance storage reclamation algorithm, ACM SIGPLAN Notices 19 (1984) 157–167. doi:10.1145/390011.808261.
1. D. Ungar, F. Jackson, Tenuring policies for generation-based storage reclamation, in: Proceedings OOPSLA ’88, volume 23, 1988, pp. 1–17.
1. M. Hertz, E. D. Berger, Quantifying the performance of garbage collection vs. explicit memory management, in: Proceedings of the 20th annual ACM SIGPLAN conference on Object-oriented programming, systems, languages, and applications, 2005, pp. 313–326.
1. R. Jones, A. Hosking, E. Moss, The garbage collection handbook: the art of automatic memory management, CRC Press, 2016.
1. R. Garner, The design and construction of high performance garbage collectors, Ph.D. thesis, The Australian National University, 2011.
1. S. M. Blackburn, P. Cheng, K. S. McKinley, Oil and water? high performance garbage collection in java with mmtk, in: Proceedings. 26th International Conference on Software Engineering, 2004, pp. 137–146. doi:10.1109/ICSE.2004.1317436.
1. S. Jayasena, M. Fernando, T. Rusira, C. Perera, C. Philips, Auto-tuning the java virtual machine, in: 2015 IEEE International Parallel and Distributed Processing Symposium Workshop, IEEE, 2015, pp. 1261–1270.
1. N. Neu, Automatic application performance improvements through VM parameter modification after runtime behavior analysis, Ph.D. thesis, University of New Brunswick, 2014.
1. P. Lengauer, H. Mössenböck, The taming of the shrew: Increasing performance by automatic parameter tuning for java garbage collectors, in: Proceedings of the 5th ACM/SPEC international conference on Performance engineering, 2014, pp. 111–122.
1. G. Vijayakumar, R. Bharathi, Predicting jvm parameters for performance tuning using different regression algorithms, in: 2022 Fourth International Conference on Emerging Research in Electronics, Computer Science and Technology (ICERECT), IEEE, 2022, pp. 1–8.
1. E. Miranda, The cog smalltalk virtual machine, in: Proceedings of VMIL 2011, 2011.
1. J.Singer,G.Kovoor,G.Brown,M.Luján,Garbagecollectionauto-tuningforjavamapreduce on multi-cores, ACM SIGPLAN Notices 46 (2011) 109–118.
1. H.Lieberman,C.Hewitt,ARealTimeGarbageCollectorBasedontheLifetimesofObjects, AI memo no 569, MIT, 1981.
1. P. Tesone, G. Polito, S. Ducasse, Profiling Code Cache Behaviour via Events, in: MPLR’21, Münster, Germany, 2021. URL: https://hal.inria.fr/hal-03332040. doi:10.1145/3475738.3480720.
1. S. Kaleba, C. Béra, A. Bergel, S. Ducasse, A detailed vm profiler for the cog vm, in: International Workshop on Smalltalk Technology IWST’17, Maribor, Slovenia, 2017. URL: https://hal.inria.fr/hal-01585754.
1. J. Singer, G. Brown, I. Watson, J. Cavazos, Intelligent selection of application-specific garbage collectors, in: Proceedings of the 6th international symposium on Memory management, 2007, pp. 91–102.
1. P. Cheng, R. Harper, P. Lee, Generational stack collection and profile-driven pretenuring, in: Proceedings of the ACM SIGPLAN 1998 conference on Programming language design and implementation, 1998, pp. 162–173. 1. T. L. Harris, Dynamic adaptive pre-tenuring, in: Proceedings of the 2nd International Symposium on Memory Management, ISMM ’00, Association for Computing Machinery, New York, NY, USA, 2000, pp. 127–136. URL: https://doi.org/10.1145/362422.362476. doi:10. 1145/362422.362476.
1. M. Jump, S. M. Blackburn, K. S. McKinley, Dynamic object sampling for pretenuring, in: Proceedings of the 4th international symposium on Memory management, 2004, pp. 152–162.
1. D. Buytaert, K. Venstermans, L. Eeckhout, K. De Bosschere, Garbage collection hints, in: High Performance Embedded Architectures and Compilers: First International Conference, HiPEAC 2005, Barcelona, Spain, November 17-18, 2005. Proceedings 1, Springer, 2005, pp. 233–248.
1. V. P. Araya, A. Bergel, D. Cassou, S. Ducasse, J. Laval, Agile visualization with Roassal, in: Deep Into Pharo, Square Bracket Associates, 2013, pp. 209–239.
