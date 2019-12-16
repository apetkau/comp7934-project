# Methods for: A comparison of BIGSI and HowDe-SBT for large-scale indexing and searching of sequence reads

* Aaron Petkau and Meghan Chua
* COMP 7934 Final Project | University of Manitoba
* December 16, 2019

This repository contains [Jupyter](https://jupyter.org/) notebooks which were used to run all the commands for performance comparisons between [HowDe-SBT](https://github.com/medvedevgroup/HowDeSBT) and [BIGSI](https://github.com/Phelimb/BIGSI) for our COMP 7934 final project.

# Stages of analysis

The different stages of analysis are listed below. Some of these stages (and their results) were unused for the final project paper.

## Preprocess data

1. Download data
    * **Notebook**: [1-download-data.nbconvert.ipynb](notebooks/1-download-data.nbconvert.ipynb)
2. Count unique kmers in downloaded data (full dataset)
    * **Notebook**: [2-kmer-cardinality.nbconvert.ipynb](notebooks/2-kmer-cardinality.nbconvert.ipynb)
3. Downsample/reduce dataset sizes
    * **Notebook**: [3-downsample-data.nbconvert.ipynb](notebooks/3-downsample-data.nbconvert.ipynb)
4. Count unique kmers in reduced dataset
    * **Notebook**: [4-kmer-cardinality-downsampled.nbconvert.ipynb](notebooks/4-kmer-cardinality-downsampled.nbconvert.ipynb)
5. Split reads into kmers with jellyfish
    * **Notebook**: [5-generate-kmers.nbconvert.ipynb](notebooks/5-generate-kmers.nbconvert.ipynb)
    
## Index and querying

6. BIGSI index
    * **Notebook k=9**: [6-bigsi-index.nbconvert.9.ipynb](notebooks/6-bigsi-index.nbconvert.9.ipynb)
    * **Notebook k=11**: [6-bigsi-index.nbconvert.11.ipynb](notebooks/6-bigsi-index.nbconvert.11.ipynb)
    * **Notebook k=13**: [6-bigsi-index.nbconvert.13.ipynb](notebooks/6-bigsi-index.nbconvert.13.ipynb)
    * **Notebook k=15**: [6-bigsi-index.nbconvert.15.ipynb](notebooks/6-bigsi-index.nbconvert.15.ipynb)
    * **Notebook k=17**: [6-bigsi-index.nbconvert.17.ipynb](notebooks/6-bigsi-index.nbconvert.17.ipynb)
7. BIGSI query
    * **Notebook**: [7-bigsi-query.nbconvert.ipynb](notebooks/7-bigsi-query.nbconvert.ipynb)
8. HowDe-SBT index
    * **Notebook k=9**: [8-howdesbt-index.nbconvert.9.ipynb](notebooks/8-howdesbt-index.nbconvert.9.ipynb)
    * **Notebook k=11**: [8-howdesbt-index.nbconvert.11.ipynb](notebooks/8-howdesbt-index.nbconvert.11.ipynb)
    * **Notebook k=13**: [8-howdesbt-index.nbconvert.13.ipynb](notebooks/8-howdesbt-index.nbconvert.13.ipynb)
    * **Notebook k=15**: [8-howdesbt-index.nbconvert.15.ipynb](notebooks/8-howdesbt-index.nbconvert.15.ipynb)
    * **Notebook k=17**: [8-howdesbt-index.nbconvert.17.ipynb](notebooks/8-howdesbt-index.nbconvert.17.ipynb)
9. HowDe-SBT query
    * **Notebook**: [9-howdesbt-query.nbconvert.ipynb](notebooks/9-howdesbt-query.nbconvert.ipynb)
    
## Comparison with BLAST

10. Assemble microbial genomes
    * **Notebook**: [10-assemble-microbial-genomes.ipynb](notebooks/10-assemble-microbial-genomes.ipynb)
11. Comparison of BIGSI and HowDe-SBT with BLAST (sensitivity/specificity)
    * **Notebook**: [11-bigsi-howdesbt-search-assembly.ipynb](notebooks/11-bigsi-howdesbt-search-assembly.ipynb)

# Dependencies

Most software contained here makes use of [conda](https://docs.conda.io) and in particular [bioconda](https://bioconda.github.io/) to install the software and dependencies.

Once this is setup, software can be installed with `conda create --name [environment] [software]` where **environment** is the name of a conda environment to install the software into and **software** is the name of the software package.

## Jupyter Lab

The main software required is [JupyterLab](https://jupyterlab.readthedocs.io) which can be installed and run with:

```bash
conda create --name jupyter jupyterlab

conda activate jupyterlab
jupyter lab
```

Once this is installed, you can load up and execute each Jupyter notebook.

## Other dependencies

These should all be listed in their respective notebooks.