# HPC Final Project - Monte Carlo Portfolio Optimization

This repository contains a portfolio optimization project using Monte Carlo simulation. It includes scripts and data required to analyze various stocks and calculate optimal portfolio performance.


## Prerequisites

Ensure the following are installed on your system:

- **Operating System**: Linux, Windows, or macOS
- **GPU**: NVIDIA GPU with CUDA capability
- **Python**: Version 3.8 or higher
- **CUDA Toolkit**: Version 11.0 or higherincluding:

## Installation

#### a. Clone this repository:

```bash
git clone https://github.com/chokez2001/HPC_FinalProject-MonteCarloPortfolioOptimization.git
cd HPC_FinalProject-MonteCarloPortfolioOptimization
``` 

#### b. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
``` 

#### c. Install CUDA Toolkit

Download and install the [CUDA Toolkit](https://developer.nvidia.com/cuda-downloads) following the instructions for your operating system. Verify the installation using:

#### d. Install Required Python Libraries
```bash
pip install quandl yfinance pandas-datareader pandas matplotlib seaborn plotly scipy
conda install -c anaconda pandas matplotlib seaborn scipy -y
conda install -c conda-forge plotly -y
conda install nvidia::numba-cuda -y
```

##  Running the Project
Launch Jupyter Notebook:


1. Open the file Monte_carlo_simmulation.ipynb.

2. Execute the cells sequentially to run the Monte Carlo simulation and visualize the results.

## Resolving the NvvmSupportError error
If you get NvvmSupportError: libNVVM cannot be found:

- Make sure you have installed cudatoolkit as above.

- Verify that the nvvm.dll library is in your PATH. For Windows systems:
 
- Navigate to the CUDA installation folder (usually C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\X.X).

- Make sure the bin subdirectory is in the system environment variables.
If the error persists, reinstall cudatoolkit or use a specific version:

```bash
conda install -c conda-forge cudatoolkit=11.2
```