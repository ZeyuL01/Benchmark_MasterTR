## Assessing NGS-based computational methods for predicting transcriptional regulators with query gene sets 
All files can be accessed from box

Link to box: https://smu.box.com/s/hlofza4oe08ob4bb4i02nu3wl2zy39zj

#### Description of files in the folder:

knockTF.zip - [knockTF](https://bio.liclab.net/KnockTFv1/) TR perturbation experiment derived genes, including the original data sourced from the knockTF database and benchmarking used top 200/600/1000 genes. 

Benchmark_Ranking_Lists.zip - Ranking lists collected, cleaned, and sorted by running each method over the collected TR perturbation gene sets.


### Commands and scripts
Command and scripts run on Ubuntu 22.04, SMU M3 high-performance computing (HPC) cluster.

#### Commands:
Please make sure the requirements are satisfied before running the command/scripts.

```
$INPUT_PATH = "/path/to/input/destination/gene_set.txt"
$OUTPUT_PATH = "/path/to/output/destination/gene_set.txt"

#BART:
bart2 geneset -i $INPUT_PATH -s hg38 --outdir $OUTPUT_PATH

#HOMER:
findMotifs.pl $INPUT_PATH human $OUTPUT_PATH

#Lisa:
lisa oneshot hg38 $INPUT_PATH --save_metadata > $OUTPUT_PATH
```

#### Scripts
For the rest of the methods, please refer to files in /Scripts/


