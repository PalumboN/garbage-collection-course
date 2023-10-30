## Tuning the Garbage Collector 

We will present a _pathological_ allocation case study. We will use the knowledge and tools from previous lectures to identify the possible causes of performance degradation. We will tune the GC to achieve a better application performance.

### Code
- At the end, the code in the _Playground_ was

  - Take the time to load a dataset
```st
[ DataFrame readFromCsv: '/Users/palumbon/Documents/GCLectures/train.csv' asFileReference ] timeToRun.
```

  - Tuning the GC

```st
"Configure the GC for loading the data set"
config := GCConfiguration readFromVM 
	fullGCRatio: 99999999999; "Simulate infinte ratio, avoid to run FullGCs when the Old Space grows"	
	growthHeadroom: 1024 * 1024 * 1024; "Grow the Old Space as much as the size of the data set"
	"tenuringThreshold: 9999999999;" "Avoid tenuring objects in the New Space -> new objects will be allocated directly in the Old Space"
	yourself.

Smalltalk vm tenuringThreshold: 9999999999.

[ config activeDuring: [ DataFrame readFromCsv: '/Users/palumbon/Documents/GCLectures/train.csv' asFileReference ] ] timeToRun.

```

### Links of interest
- Datasets:
  - `test.csv` https://www.kaggle.com/datasets/rahulbanerjee123/aws-product-length?resource=download
  - `train.csv` https://www.kaggle.com/datasets/rahulbanerjee123/aws-product-length?resource=download
  - `protein.csv` https://www.kaggle.com/datasets/antoninadolgorukova/proteinrna-vs-rna-spearman-correlation-data?select=Prot-RNA_corr_63gr.csv
- Repos:
  - DataFrame https://github.com/PolyMathOrg/DataFrame
  - Pharo VM Tuning https://github.com/pharo-project/pharo-vm-tunning
- Paper about the DataFrame experience (+ description of the Pharo GC parameters): https://inria.hal.science/hal-04225588v1/document


### Practice
- Repeat the experiment and validate the numbers published in the paper ;)
- Tryto improve the performance of your programs using the presented methodology.
