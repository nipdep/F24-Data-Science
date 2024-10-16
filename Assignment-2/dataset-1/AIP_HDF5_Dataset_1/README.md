# Dataset for Medical LLaMa Performance Comparison with Model Scale

## Overview

The goal of the dataset was to analyze and understand the performance variations of large language models (LLMs) in the medical domain,specifically focusing on the effect of model architecture and training data on performance metrics such as reliability and inference time. 
This would allow for a detailed comparison of competing medical LLMs, helping researchers make informed decisions regarding model selection based on the trade-offs between speed, accuracy, and scalability.

## Dataset Structure

The dataset is stored in an HDF5 file with the following structure:

- `content/`: Information about the evaluated LLMs
  - `medical_llama_performance_dataset.h5`: The dataset evaluates and compares the performance of LLAMA-based medical LLMs, focusing on the impact of model architecture and training data on key performance metrics.

- `metadata/`: Information about the evaluation datasets
  - `structural_metadata.xml`: Include information about the HDF5 file structure, groups, and datasets.
  - `descriptive_metadata.xml`: Add details about what the data represents, its origin, and its significance.
  - `preservation_metadata.xml`: Document the history of the dataset, including its creation and any modifications.

- `manifest.txt`: List all files in the package with their checksums.

- `README.md`: README file explaining the contents and structure of the AIP.


## Usage

To access the data, use the h5py library in Python:

```python
import pandas as pd

df = pd.read_hdf('./content/medical_llama_performance_dataset.h5', 'data')
df.head()
```