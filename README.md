# **ForAlign: A TLS-DLS Forest Point Cloud Registration Algorithm**
![ForAlign Overview](image/foralign.png)

ForAlign is a Python-based algorithm designed for automated registration of **terrestrial laser scanning (TLS)** and **drone laser scanning (DLS)** point clouds in forest environments. The algorithm leverages structural features for robust alignment and operates within a **Jupyter Notebook** environment, primarily utilizing the [Open3D library](https://github.com/isl-org/Open3D).  

For compatibility, please use **Python 3.8 - 3.11**.

---

## **Algorithm Overview**
ForAlign consists of two key registration stages:  

1. **Coarse Alignment (matching_optimization.ipynb)**: Identifies and matches trees across TLS and DLS point clouds using structural graph-based constraints.  
2. **Fine Alignment (finetune_optimization.ipynb)**: Refines the registration by optimizing the transformation through a voxel-based point-to-mesh approach.  

Each stage is implemented in separate files, allowing users to execute the **full pipeline** or run specific alignment steps independently.

Each notebook includes detailed documentation and comments to guide users through the process.

**Note:** When using **Coarse Alignment**, ensure that the **Digital Terrain Model (DTM) is separated**, with TLS and DLS each containing **ground** and **off-ground** point clouds (e.g., using the [CSF](https://github.com/jianboqi/CSF) filter). The point clouds must be in **PCD format**.

---

## **Environment**
Before running **ForAlign**, ensure that you have the necessary dependencies installed.  
If you encounter compatibility issues, refer to the tested versions listed below.

### **Required Dependencies**  
Install the required libraries using the following command:
```bash
pip install open3d==0.18.0 numpy==1.24.3 matplotlib==3.7.1 scipy==1.15.1 \
scikit-learn==1.3.0 hdbscan==0.8.33 networkx==3.1 pulp==2.8.0 rasterio==1.3.9 pandas==2.0.3
```

### **Tested Environment & Library Versions**  
ForAlign has been tested in the following environment:

- **Python Version**: `3.11.11` (Anaconda)
- **Operating System**: `Windows 64-bit (MSC v.1929 AMD64)`

| Library        | Version |
|---------------|---------|
| Open3D       | 0.18.0  |
| NumPy        | 1.24.3  |
| SciPy        | 1.15.1  |
| Scikit-learn | 1.3.0   |
| HDBSCAN      | 0.8.33  |
| PuLP         | 2.8.0   |
| Rasterio     | 1.3.9   |
| Pandas       | 2.0.3   |

If you experience any issues, consider using the tested versions above.

---

## **Datasets**
To complement publicly available forest point cloud datasets, we provide two **real-world TLS and DLS datasets** collected in Japanese plantation forests, along with **three synthetic datasets**.  
Each dataset contains TLS and DLS point clouds of the same forest scene.  

The synthetic datasets were generated using:
- **[Arbaro](https://github.com/wdiestel/arbaro)** for simulating 3D tree models.
- **[Blender](https://www.blender.org/)** for constructing 3D forest environments.
- **[Helios++](https://github.com/3dgeo-heidelberg/helios)** for LiDAR simulation.

To access the datasets, please fill out the following [survey form](https://docs.google.com/forms/d/e/1FAIpQLSeCLMzWzCvZ4l-i3MPGoaAbRbye_4djHRF8Xr-QXa2coF7WCQ/viewform?usp=dialog).

---

