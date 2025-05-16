
# fMRI Generalisation
The goal of this project is to understand if the number of participate affects Generalization of the model's. The dataset comes from the [CNeuroMod](https://www.cneuromod.ca/) dataset, and consists of multimodal movie stimuli and corresponding whole-brain time series fMRI responses of four subjects. A subset of CNeuroMod's data which includes almost 80 hours of multimodal movie stimuli and corresponding fMRI responses. The stimuli consist of movie visual frames, audio samples, and time-stamped language transcripts. The neural data consist of whole-brain fMRI responses for four CNeuroMod subjects (sub-01, sub-02, sub-03 and sub-05), normalized to the Montreal Neurological Institute (MNI) spatial template ([Brett et al., 2002](https://doi.org/10.1038/nrn756), and processed as time series whose signal is assigned to 1,000 functionally defined brain parcels ([Schaefer et al., 2018](https://doi.org/10.1093/cercor/bhx179).
For this experiement sub-05 was removed from the training and is treated as the test set. 
The workflow includes data preprocessing, feature alignment, model training, and validation.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Functions Overview](#functions-overview)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/fmri-generalisation.git
   cd fmri-generalisation

2. Install the required Python packages
   ```bash
   pip install -r requirements.txt

3. Ensure you have the necessary data files and feature embeddings from:
[Algonauts challenge 2025](https://algonautsproject.com/)


## Usage
1. Open the generalisation.ipynb notebook in 
Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook generalisation.ipynb

2. Follow the steps in the notebook to:

    - Load stimulus features and fMRI responses.
    - Align features with fMRI samples.
    - Train an encoding model using Ridge regression.
    - Validate the model and compute encoding accuracy.

3. Run the final cell to visualize the encoding accuracy on a 3D brain atlas.

## Project Structure 
 ```bash
fmri-generalisation/
├── data/
│   └── algonauts_2025.competitors  # Directory containing stimulus features and fMRI data
├── [generalisation.ipynb](https://github.com/genandlam/fmri-generalisation/blob/main/generalisation.ipynb)           # Main notebook for the project
├── requirements.txt                 # Python dependencies
└── README.md                       # Project documentation
