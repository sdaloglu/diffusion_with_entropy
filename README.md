# Application of Machine Learning - Coursework Assignment


## Description

This project contains the code required to address the coursework questions for the Application of Machine Learning. The goal of this project is to demonstrate a practical approach to training Denoising Diffusion Probabilistic Models, highlighting the impact of various hyperparameters on model performance through established metrics and visual inspection of generated samples. Moreover, it introduces an innovative custom degradation technique that integrates entropy calculations with noise modulation, offering a nuanced approach to model training.


## Installation

The first step is to clone the remote GitLab repository on a local machine. Then, the required packages to run this project that are listed in `requirements.txt` can be installed via:


```bash
pip install -r requirements.txt
```



## Usage

The model and the training procedure is provided in a jupyter notebook. In order to run the notebook, the following command can be used from a terminal:

```bash
jupyter nbconvert --execute --to script DDPM.ipynb
```


This command will run the notebook and then convert it to a Python script named `DDPM.py`



## Changing the hyperparameters

* To change the noise schedule of the model, adjust the `noise_schedule` variable inside both `DDPM` and `DES` class definitions.

* To change the capacity of the U-Net to an increased capacity, replace `ddpm` variable with `ddpm_capacity`.

* To change the degradation method, and use DES instead of DDPM, replace `ddpm` variable with `des` variable.



## Trained Models and Samples Generated

The already trained models and samples generated are placed in the following directories:

* `contents_all` directory has the initial default model trained for 100 epochs, with generated images
* `contents_custom` directory has the custom/cosine noise schedule model trained for 50 epochs, with generated images.
* `contents_lin` directory has the linear noise schedule model trained for 50 epochs, with generated images. This is the same as the `contents_all` but trained for less epochs.
* `contents_geo` directory has the geometric noise schedule model trained for 50 epochs, with generated images.
* `contents_custom_largen_hidens` directory has the linear noise schedule model with increased U-Net capacity trained for 50 epochs, with generated images.
* `contents_entropy` directory has the linear noise schedule model with the custom degradation strategy (DES) implemented and trained for 50 epochs, with generated images.


## Model and Plot savings

The noise schedule plot used in the report, will be saved inside the `plots` directory. The plotting of the loss functions are available for all the modes, preferred comparison can be made by commenting the remaining ones. Loss function plots are also saved inside the `plots` directory.

The metric plots for SSIM and PSNR are saved inside the `plots` directory as well. The FID scores table is saved as `fid_scores.csv` inside the `plots` directory



## The use of generative A.I.

ChatGPT 3.5 was used for suggesting alternative wordings, grammar suggestions, and proofreading while writing the report. The following prompts were used during this process

```
How can I write this equation in LaTeX format? <input equation>
```
```
Provide BibTex citation format for this website  <input website>
```
```
How to represent/write <input symbol> in LaTeX?
```
```
What is another word for <input word>?
```
```
Is this sentence grammatically correct? <input sentence>
```
```
Is this paragraph clear for a reader? <input paragraph>
```
```
How to rephrase this sentence to make it more clear? <input sentence>
```
For the report writing, the outputs were partially adapted in a way that only alternative wordings were used and not the whole output while rephrasing the discussion parts of the report. The LaTex code for equations was adapted from the suggestion. The suggestions for BibTeX citations are also adapted.

Furthermore, the suggestions from the autocomplete feature of `GitHub Copilot` were utilized during the documentation of the software, and code development of the project such as adjusting the style of the plots generated.

## Authors
Sabahattin Mert Daloglu

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) for details.

