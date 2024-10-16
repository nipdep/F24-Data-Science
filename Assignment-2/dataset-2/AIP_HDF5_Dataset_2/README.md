# RPI Foot-traffic dataset

## Overview

This dataset captures foot traffic data across various locations within Rensselaer Polytechnic Institute (RPI) University, manually collected by a single investigator. The investigator recorded foot traffic at key entry points around campus buildings, pathways, and common areas through direct observation.

## Dataset Structure

The dataset is stored in an HDF5 file with the following structure:

- `content/`: Information about the evaluated LLMs
  - `foot_traffic_dataset.h5`: The dataset is stored in HDF5 format and includes information on the time, location, and volume of foot traffic over specified periods, providing insights into pedestrian flow across campus areas.

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

df = pd.read_hdf('./content/foot_traffic_dataset.h5', 'data')
df.head()
```