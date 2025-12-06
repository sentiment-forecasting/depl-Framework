### 1. Code Explanation
The `data` folder contains the datasets used in this paper. The `code` folder contains the code used in the paper. To replace exchange rate data and sentiment labels, please find the corresponding datasets and labels in the `data` folder.

- `correlation_analysis.ipynb`: Correlation analysis based on exchange rate returns, average sentiment scores, and sentiment polarity labels.
- `EMD decomposition.ipynb`: EMD decomposition performed on raw exchange rate data.
- `main_feature.ipynb`: Prediction code based on the DEPL framework, combining exchange rate data and sentiment labels for prediction.
- `main_non_feature.ipynb`: Prediction code based on the DEPL framework, using only exchange rate data for prediction.

#### Usage Instructions:
- **Perform EMD decomposition on raw exchange rate data**:  
  Run `EMD decomposition.ipynb`.

- **Analyze correlation between exchange rate returns and sentiment features**:  
  Run `correlation_analysis.ipynb`.  
  The exchange rate dataset can be replaced at line 137, and the saved file name can be replaced at line 177 of the code.

- **Predict exchange rates using only exchange rate data based on the DEPL framework**:  
  Run `main_non_feature.ipynb`.  
  The exchange rate dataset can be replaced at line 531, and parameters can be adjusted at lines 435-439 of the code.

- **Predict exchange rates by combining exchange rate data and sentiment labels based on the DEPL framework**:  
  Run `main_feature.ipynb`.  
  The exchange rate dataset can be replaced at line 541, parameters can be adjusted at lines 445-449, and sentiment labels can be replaced at line 84 of the code.  
  In particular, to optimize model performance, adjust the parameters in `main_feature.ipynb` and `main_non_feature.ipynb`.


### 2. Environment Configuration and Dependency Notes
#### Hardware Requirements
- GPU: NVIDIA GPU (CUDA-compatible) – recommended for accelerated training
- Memory: ≥8GB RAM
- Storage: ≥2GB available space

#### Software Environment
- Operating System: Windows 10/11, Linux Ubuntu 18.04+, or macOS 10.14+
- Python: 3.8-3.10 (3.9 recommended)
- Jupyter Notebook/JupyterLab

#### Required Python Packages and Versions
```
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
torch>=1.9.0
torchvision>=0.10.0
PyEMD>=1.4.0
pyswarm>=1.3.0
matplotlib>=3.5.0
scipy>=1.7.0     
```

#### Jupyter Environment
```
jupyter>=1.0.0
ipykernel>=6.0.0
```

#### Install All Dependencies via pip
```bash
pip install numpy>=1.21.0 pandas>=1.3.0 scikit-learn>=1.0.0
pip install torch>=1.9.0 torchvision>=0.10.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install PyEMD>=1.4.0 pyswarm>=1.3.0 matplotlib>=3.5.0
```

#### Or Install via conda
```bash
conda install numpy pandas scikit-learn matplotlib
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
pip install PyEMD pyswarm
```

### Code File Structure Requirements
```
project_root/
│
├── main.ipynb                    # Main Jupyter Notebook file
├── EURUSD_DPSK_final.csv         # Exchange rate data file
├── requirements.txt              # List of dependencies
└── all_feature/                  # Result output directory
    └── prediction_results/       # Prediction result files
```

### Running Instructions
1. Ensure all dependencies are installed correctly.
2. Place the CSV files from the `data` folder in the same directory as the notebook files.
3. Execute all code cells in sequence.
4. Results will be automatically saved to the relevant directory (the save directory can be adjusted).


```python

```
