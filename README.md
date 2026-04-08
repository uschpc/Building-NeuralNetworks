# CARC Workshop on Building-NeuralNetworks

### About
The material in this repo contains workshop materials related to building neural networks for deep learning applications. 

### Software Environment Setup
(Make sure you are connnected to USC secure wireless or VPN first)
First login to CARC OnDemand: https://ondemand.carc.usc.edu/ and request a 'Discovery Cluster Shell Access' within OpenOnDemand. 

We will use Conda to build software packages. If it is the first time you are using Conda, make sure you follow the guide of how to use Conda with this link: https://www.carc.usc.edu/user-guides/data-science/building-conda-environment
```bash
salloc --partition=gpu --gres=gpu:1 --cpus-per-task=8 --mem=32GB --time=1:00:00 
```
```
module purge
module load conda
python carc_conda_setup.py
```
When you finish the installation, type 'exit' to exit from the interactive session.
```bash
git clone https://github.com/uschpc/Building-NeuralNetworks.git
cd Building-NeuralNetworks
```


