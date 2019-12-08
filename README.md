# comp7934-project

Each Jupyter notebook can be run using:

```bash
jupyter nbconvert --to notebook --ExecutePreprocessor.timeout=None --execute [notebook.ipynb]
```

# Stages of analysis

The different stages of analysis are listed below. These include a reference to the **Master Notebook**, the main notebook used to execute all the operations. As well, the **Results Notebook**, this notebook was constructed from the **Master** and contains the output of the results of execution.

1. Download data
    * **Master Notebook**: [1-download-data.ipynb](1-download-data.ipynb)
    * **Results Notebook**: [2-download-data.ipynb](2-download-data.ipynb)
2. Count unique kmers
    * **Master Notebook**: [2-count-kmers.ipynb](2-count-kmers.ipynb
    * **Results Notebook**: [2-count-kmers.nbconvert.ipynb](2-count-kmers.nbconvert.ipynb)