1. Download the VM based on your OS and architecture.

2. Open a terminal and run the VM passing an image file

```bash
# On MAC

./Pharo.app/Contents/MacOS/Pharo "<IMAGE_FILE>" --interactive

# On Linux

./pharo "<IMAGE_FILE>" --interactive
```

  - If you want to evaluate some Pharo code without opening the interactive world

```bash
<VM_FILE> "<IMAGE_FILE>" eval "<CODE>"

# For example:

./pharo "./Pharo 11/Pharo 11.image" eval "1+1"

# The result will be printed on the console
```

3. A file `scavenge.log` will appear in the current directory of your terminal.

4. Download the image `P11-gc-charts` and open it (you can use the PharoLauncher for this).

5. Inside the image, open a Workspace, create a file reference to your `scavenge.log` file and explore the `GCChart` class to plot some charts.

Example:
```st
logFile := '/Users/palumbon/Desktop/cerciras/Riga-2023/scavenge.log' asFileReference.

chart := GCChart simple.

chart addProfile: logFile named: 'Test'.

chart plotScavengeTimes.
```

For more info about the `GCChart` read the description of [this PR](https://github.com/tesonep/benchy/pull/23).

-------------

### This approach was using for tuning the Pharo Garbage Collector in applications with _pathological allocation patterns_.
The paper is [here](https://github.com/ESUG/esug.github.io/blob/source/2023-Conference/iwst/papers/IWST_2023_paper_6.pdf)!
