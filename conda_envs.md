# Conda Environments

> **Note:** These environments will be updated periodically based on user feedback and official package updates.

| Name | Kernel Name | Version | Description |
| ---- | ----------- | ------------------ | ----------- |
|`base`| Python | Python 3.12.8 | Default Python environment with scientific computing libraries |
|`pytorch`| Python (Pytorch) | Python 3.11.8 | Deep learning environment focused on PyTorch and related tools |
|`r_env`| R (4.3) | R 4.3.3 | R statistical computing environment with comprehensive package selection |

## `base` Environment (Python 3.12.8)

```
python=3.12.8
numpy=2.2.2
pandas=2.2.3
scipy=1.15.1
matplotlib=3.10.0
seaborn=0.13.2
scikit-learn=1.6.1
jupyterlab=4.3.4
jupyter=1.1.1
plotly=5.24.1
ipykernel=6.29.5
statsmodels=0.14.4
nltk=3.9.1
xgboost=2.1.4
lightgbm=4.6.0
networkx=3.4.2
```

## `pytorch` Environment (Python 3.11.8)

```
python=3.11.8
numpy=2.0.2
pandas=2.2.3
scipy=1.15.2
matplotlib=3.10.0
seaborn=0.13.2
scikit-learn=1.6.1
torch=2.6.0
torchvision=0.21.0
torchaudio=2.6.0
transformers=4.49.0
tensorflow=2.18.0
keras=3.8.0
ipykernel=6.29.5
pytorch-lightning=2.5.0
huggingface-hub=0.29.1
spacy=3.8.4
wandb=0.19.7
mlflow=2.20.2
xgboost=2.1.4
lightgbm=4.6.0
shap=0.46.0
networkx=3.4.2
nltk=3.9.1
```

## `r_env` Environment (R 4.3.3)

```
r-base=4.3.3
r-essentials=1.4
r-tidyverse=2.0.0
r-data.table=1.15.4
r-dplyr=1.1.4
r-ggplot2=3.5.1
r-caret=6.0_94
r-plyr=1.8.9
r-randomforest=4.7_1.2
r-rmarkdown=2.27
r-knitr=1.48
r-shiny=1.8.1.1
r-plotly=6.0.0
r-sf=1.0_16
r-glmnet=4.1_8
r-quantmod=0.4.26
r-xts=0.14.1
r-devtools=2.4.5
r-readxl=1.4.3
r-fixest=0.12.1
r-sandwich=3.1_0
r-lava=1.8.1
r-mass=7.3_60.0.1
r-nlme=3.1_167
r-survival=3.8_3
r-e1071=1.7_14
r-rgdal=1.6_7
r-sp=2.1_4
```

### Installing Additional R Packages

If you need R packages that aren't included in the pre-configured environment, you can install them in your user directory:

1. Activate the R environment and start R:
   ```bash
   conda activate r_env
   R
   ```

2. Use the `install.packages()` function to install your desired package:
   ```r
   install.packages("package_name")
   ```

3. When prompted with a message that the library path is not writable, select the option to use a personal library instead (usually by typing `yes`).

4. R will create a directory in your home folder (typically at `~/R/x86_64-pc-linux-gnu-library/4.3`) and install the package there.

5. These personally installed packages will be available in your future R sessions without needing to reinstall them.
