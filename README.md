# chloroplast-assembly-optimization

# 🧬 Chloroplast Genome Assembly Optimization


## 📌 Overview

This project focuses on the **assembly of chloroplast genomes from short-read sequencing data**, with the goal of identifying optimal parameters to improve assembly quality.

The study uses *Helianthus niveus* and *Helianthus praecox* as test cases and explores how **coverage, k-mer size, assembly tools, and reference genome selection** affect the final assembly.


## 🎯 Objectives

* Assemble chloroplast genomes from Illumina short reads
* Optimize assembly parameters (coverage and k-mer)
* Compare different assembly tools
* Evaluate the impact of evolutionary distance of the reference genome
  

## 🧪 Dataset

Sequencing data were obtained from the SRA repository:

* *Helianthus niveus*: `SRR8896549`
* *Helianthus praecox*: `SRR3492254`

Reference genome:

* *Helianthus debilis* (chloroplast genome)
  

## ⚙️ Pipeline

The workflow consists of the following steps:

1. **Download reads**

   * SRA Toolkit

2. **Preprocessing**

   * Adapter trimming: `fastq-mcf`

3. **Read mapping**

   * `Bowtie2`

4. **Processing alignments**

   * `Samtools`

5. **Coverage calculation**

   * `Bedtools`

6. **Extraction of chloroplast reads**

7. **Assembly**

   * `ABySS`
   * `SOAPdenovo`
     

## 🔬 Optimization Strategy

### Parameters tested:

* **Coverage** (subset of reads)
* **k-mer size**
* **Assembly tool**

### Evaluation metrics:

* Number of contigs
* Assembly length
* N50
* Coverage

## 📊 Results

* Initial assemblies were fragmented
* Optimization of parameters significantly improved results
* Best assembly obtained:

  * ~151 kb total length
  * 2 contigs
* Choice of a **phylogenetically close reference genome** improved mapping and assembly quality
  

## 📈 Key Insights

* k-mer size strongly affects contiguity
* Coverage must be balanced (too high/low worsens assembly)
* Different assemblers require different parameter tuning
* Reference genome selection is critical
  

## 📁 Project Structure

```
.
├── scripts/
├── docs/
│   └── report.pdf
├── results/
└── README.md
```



## 🚀 Future Improvements

* Full automation of the pipeline
* Containerization (Docker)
* Visualization of assembly graphs
* Extension to additional species


## 📚 Reference

See the full report in `/docs`.


## 👩‍🔬 Author

Michela Dell’Alma
