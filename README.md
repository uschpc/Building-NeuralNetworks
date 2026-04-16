# CARC Workshop on Building-NeuralNetworks

### About
The material in this repo contains workshop materials related to building neural networks for deep learning applications. 

### Software Environment Setup
(Make sure you are connnected to USC secure wireless or VPN first)
First login to CARC OnDemand: https://ondemand.carc.usc.edu/ and request a 'Discovery Cluster Shell Access' within OpenOnDemand. 

We will use Conda to build software packages. Please follow the instructions below on how to install packages (carc_conda_setup.py will automatically install common packages such as PyTorch, Matlotlib, Pandas and etc in the conda environment):
```bash
salloc --partition=gpu --gres=gpu:1 --cpus-per-task=8 --mem=32GB --time=1:00:00 
```
```
module purge
module load conda
git clone https://github.com/uschpc/Building-NeuralNetworks.git
cd Building-NeuralNetworks
python carc_conda_setup.py
```


