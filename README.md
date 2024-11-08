# CARC Workshop on Building-NeuralNetworks

### About
The material in this repo contains workshop materials related to building neural networks for deep learning applications. 

### Software Environment Setup
First login to CARC OnDemand: https://ondemand.carc.usc.edu/ and request a 'Discovery Cluster Shell Access' within OpenOnDemand. 

We will use Conda to build software packages. If it is the first time you are using Conda, make sure you follow the guide of how to use Conda with this link: https://www.carc.usc.edu/user-guides/data-science/building-conda-environment
```bash
salloc --partition=gpu --gres=gpu:1 --cpus-per-task=8 --mem=32GB --time=1:00:00 
```
```
module purge
module load conda
mamba init bash
source ~/.bashrc
module purge
```
```
mamba create --name torch-env
mamba activate torch-env
mamba install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
mamba install line_profiler --channel conda-forge   #optional, needed if you want to use line_profiler function within your code
```

### Install Jupyter Kernel
Follow the link to CARC Jupyter Kernel documentation: https://www.carc.usc.edu/user-guides/hpc-systems/software/jupyter-kernels and Look for the 'Conda' Section to install Jupyter Kernel: 
```bash
mamba install -c conda-forge ipykernel   # This will install ipykernel inside your Conda environment
python -m ipykernel install --user --name torch-env --display-name "torch-env"     #This will link your Conda environment to OpenonDemand Jupyter Notebook Kernel
```
When you finish the installation, type 'exit' to exit from the interactive session.
```bash
module load gcc/11.3.0
module load git
git clone https://github.com/uschpc/Building-NeuralNetworks.git
cd Building-NeuralNetworks
```


