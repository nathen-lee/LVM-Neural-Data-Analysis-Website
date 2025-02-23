<br>
<p align="center">Mohamed Elshazly: melshazly@ucsd.edu</p>
<p align="center">Nathen Lee: nal008@ucsd.edu</p>
<p align="center">Charlie Gillet: cgillet@ucsd.edu</p>
<p align="center">Mentor: Mikio Aoi maoi@ucsd.edu</p>

<a href="https://github.com/Charlie-279/LVM-Neural-Data-Analysis"> Written Report (still need to replace this with actual link to paper)</a>
<br>
<a href="https://github.com/Charlie-279/LVM-Neural-Data-Analysis">Github Code Repository </a>
<br>

## Introduction
As methods for recording neural data advance rapidly in both volume and speed \citep{buccino2022spike}, neurophysiologists face increasing challenges in developing innovative techniques to assess and sort incoming spike signals (neuron firing rates) and inferring relationships between neural activities across different brain regions. We seek to create and utilize a method for extracting shared and independent latent features that accurately represent interpretable neural population dynamics across distinct brain regions.

The model we wish to construct builds on four main core components that serve as the foundation, allowing it to operate as we desire it to. These four components are: the FA framework, AEVB framework, PCCA, and GPs. These components will be the key pieces used to build our two-step model pipeline that we will be inputting our data into: variational Gaussian Process Factor Analysis model (vGPFA) and probabilistic Canonical Correlation Analysis (pCCA) model. By using these core principles, our latent variable model will be able to extend the principles of factor analysis to extract latent representations within neural data to provide more interpretable firing rate dynamics than other current methods. 

## Model Hierarchy Pipeline
### IBL Data
Using the International Brain Laboratory, we aim to analyze the latent behaviors of multiple regions of the brain in mice during standardized experiments. In these experiments, mice, with up to two probes recording 384 channels inserted into their brains, undergo a decision-making task where they are shown a stimulus of several different contrast strengths and  is to move a wheel to center the stimulus on a screen. The IBL database contains large amounts of neural data (about 621,733 neurons) collected from 699 insertions of Neuropixel probes using 139 different mice over many experiment trials. These experiments give insight into regions and times in the brain that show sensitivity to stimulus, movement, reward, vision, and decision making. 

### Variational Gaussian Process Factor Analysis (vGPFA) Model
The first model our data will be put through is a variational Gaussian Process Factor Analysis (vGPFA) model, which is primarily used in neuroscience to decode neural data into a more interpretable lower-dimensional latent space governed by Gaussian Processes. This model uses necessary imports from essential libraries such as NumPy, SciPy, Matplotlib, and the vGPFA-specific library developed by Yuan Zhao and Il Memming Park to handle computations and visualizations.

### Probabilistic Canonical Correlation Analysis (pCCA) Model
The next and final step of our pipeline involves a probabilistic Canonical Correlation Analysis (pCCA) model. After the IBL data is collected and cleaned, it will be first put through the vGPFA model to smoothen and move the data to a lower-dimensional latent space. Then, the vGPFA model's output is used as the input to the pCCA model in order to conduct the analysis. In the field of neuroscience, pCCA is typically used to model latent variables that explain the variability between two or more modalities of data, which helps to understand complex neural dynamics.

## Results

## Conclusions
