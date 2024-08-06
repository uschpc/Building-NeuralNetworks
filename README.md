# CARC Workshop on Building-NeuralNetworks

### About
The material in this repo contains workshop materials related to building neural networks for deep learning applications. 

### Software Environment Setup
If it is the first time you are using Conda, make sure you follow the guide of how to use Conda with this link: https://www.carc.usc.edu/user-guides/data-science/building-conda-environment
```bash
$ ssh <YourNetID>@discovery.usc.edu  # VPN required if off-campus
$ salloc --partition=gpu --gres=gpu:1 --cpus-per-task=8 --mem=32GB --time=1:00:00
$ mamba create --name torch-env
$ mamba activate torch-env
$ mamba install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
$ mamba install line_profiler --channel conda-forge   #optinally, needed if you want to use line_profiler function within your code 
$ git clone https://github.com/uschpc/Building-NeuralNetworks.git
$ cd Building-NeuralNetworks
