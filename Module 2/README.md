## Generational Garbage Collector 

The lecture will introduce High-Performance Garbage Collectors, particulary the Generational Garbage Collector algorithm. We will describe how the GC is implemented inside the Pharo Virtual Machine and create some programs to stress the GC in different ways.

### Code
- At the end, the code in the _Playground_ was

```st
pepita := Swallow new.
pepita areYouTired.
pepita fly: 30.

Smalltalk garbageCollect. "FullGC"
Smalltalk garbageCollectMost. "Scavenge"

Smalltalk vm totalGCTime.

Smalltalk vm incrementalGCCount. "229" "233" "321" "452" "461"

Smalltalk vm fullGCCount. "1" "1" "1" "2" "2" "2" "2" "2" "4"

Smalltalk vm tenureCount. "72007" "72007" "72007" "72016" "72016" "145066"

birds := OrderedCollection new.
birds add: pepita.
birds.
1 to: 1000000 do: [ :index | birds add: Swallow new ].
```

### Links of interest
- Paper about Generational Garbage Collectors: https://www.researchgate.net/publication/220404180_An_Adaptive_Tenuring_Policy_for_Generation_Scavengers
- Book about High-Performance Garbage Collectors (complementary to this course): https://openresearch-repository.anu.edu.au/bitstream/1885/9053/1/02WholeThesis_Garner.pdf

### Practice
- Execute programs to stress the Garbage Collectors in different ways.
- Validate the expected behaviour using the VM statistics.
