## Tuning the pathological allocation patterns

Now it's time to apply what we learn!

- Select one (or many) application developed in this course and analyse the impact of the GC on its performance.
  - Check the total GC overhead
  - Profile it

Then,
- For pathological cases (what we are looking for), 
  - Analyse the profile data to identify possible causes of performance degradation 
  - Tune the GC for solving them
- For good cases
  - Explain why the default values in the GC parameters performs efficiently
  - Tune the GC to make it a pathological case! 😈