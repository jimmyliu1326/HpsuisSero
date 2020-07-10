# HpsuisSero

## Description
This pipeline is designed to rapidly infer Haemophilus parasuis serotype from Oxford Nanopore Data by first assemblying a draft genome using Flye followed by genome polishing with medaka. The processed assembly is subsequently queried against the Cps Blast Database to determine isolate serotype. An additional feature identification step is required to resolve between serotype 5 and 12.

## Usage
<pre>
<b>Required arguments:</b>
-i  input raw reads
-o  path to output directory
-s  sample name

<b>Optional arguments:</b>
-h|--help       display help message
-t|--threads    number of threads [4]

<b>Example Command Line:</b>
HpsuisSero.sh -s Sample_1 -i /path/to/Sample_1.fastq -o /path/to/output
</pre>

## Conda Installation
The recommended method of installation for this pipeline is with Conda. Set up a new conda environment and run:

```
conda install -c bioconda hpsuissero
```

### Dependencies
* Medaka >= 1.0.1
* Blast >= 2.6
* Flye >= 2.7.1