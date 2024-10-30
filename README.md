# ForestAlign: A TLS-DLS Forest Point Cloud Registration Algorithm

ForestAlign is a Python-based algorithm designed for automated registration of forest point clouds from terrestrial and drone platforms using structural features. The project is provided as a Jupyter Notebook and mainly relies on the [Open3D library](https://github.com/isl-org/Open3D). For compatibility, please use Python **3.8 - 3.11**.

## Algorithm Overview
ForestAlign is composed of two main steps:
1. **Coarse Alignment**: Matches the positions of trees across different platforms.
2. **Fine Alignment**: Refines the alignment of TLS and DLS point clouds after Coarse Alignment.

Each stage is separated into individual files, allowing users to either run the full alignment process or specific steps.

## Installation
Before running ForestAlign, please install the following libraries:

### Core Dependencies
These libraries are required for both the Coarse and Fine Alignment steps:
- `open3d>=0.17.0`
- `numpy>=1.24.3`
- `matplotlib>=3.7.1`
- `scipy>=1.11.1`
- `scikit-learn>=1.2.2`
- `hdbscan>=0.8.29`
- `networkx>=3.1`

### Additional Libraries for Coarse Alignment
- `rasterio>=1.3.8`

### Additional Libraries for Fine Alignment
- `statsmodels>=0.14.0`
- `shapely>=2.0.1`

## Usage
After installing the required libraries, you can run the algorithm by following the instructions in the Jupyter Notebook files for each alignment stage. 

For further details on each stage, refer to the comments and documentation provided within the notebook files.

## License
## Citation

