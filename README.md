

# Slides

[Slides Link](https://microsofteur-my.sharepoint.com/:p:/g/personal/victorgar_microsoft_com/ES6COVnaLvpDr77-tNZ9yzsBNZGs-nC8E4C-gRdo2QTiBw?e=A8Xs5t)

# Probai Summer School 🌞 - Deep Generative Models

## Course Overview
### Part 1
- Introduce the data
    - Explain how data is structured (x,h) (small subset of QM9)
    - Visualize and plot
- Introduce the diffusion model for molecule generation (EDM) (sync with Rianne)
    - Explain how are we going to generate molecules using a diffusion model
- Implementing diffusion model for molecule generation
    - They will have to fill gaps in code to run a training pipeline.
    - Train a small diffusion model.
- Sample using the trained diffusion model.
    - i.i.d. Sample
    - Visualize Samples.
    
### Part 2
- Introduce MD
- Introduce relation of diffusion model with MD (Two for One)
- Train very simple conditional model on a small molecule
- Implement Brownian dynamics
- Run and visualize dynamics


## Tools
- Visualizing tool (ASE?)

## TO DO:

- Make visualization code.
- Curate QM9 into MicroQM9.
- Provide a whole training and dataloading pipeline.
    - Training loop
    - Training step / update
    - Loss
    - Sampling process
    - Data and dataloader
    - MD 
 - Get data for the MD exercise.


### Set up environment

TODO: test if it works
```bash
wget -O ./miniconda.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash ./miniconda.sh -b -f -p /usr/local
rm miniconda.sh
conda install mamba -n base -c conda-forge
mamba env create --file=environment.yml
```

### Code structure

```
.
├── README.md
├── environment.yml
├── notebooks
│   └── workshop_notebook_1.ipynb
├── src
│   ├── __init__.py
│   ├── data
│   │   ├── __init__.py
│   │   ├── dataset.py
│   │   └── preprocessing.py
│   ├── models
│   │   ├── __init__.py
│   │   ├── ddpm.py
│   │   └── layers.py
│   ├── training
│   │   ├── __init__.py
│   │   ├── training_loop.py
│   │   └── utils.py
│   └── evaluation
│       ├── __init__.py
│       └── metrics.py
├── configs
│   └── default_config.yml
└── scripts
    ├── train.py
    ├── pre_process_data.py
    └── evaluate.py
```

- `notebooks`: This directory contains Jupyter Notebooks that the students will have to fill.
- `src`: This directory contains the source code for the project.
- `configs`: This directory contains configuration files (e.g., in YAML format) for different scenarios
- `scripts`: This directory contains Python scripts for running the training and evaluation pipeline. These scripts will import the necessary components from the src directory and use the configuration files to set up the experiments.


