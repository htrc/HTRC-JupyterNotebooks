# HTRC-JupyterNotebooks

#### Downloading this repository
This repository contains Jupyter Notebooks containing Python code that performs text analytics algorithms as well as detailed annotations and instructions for running the code. To download this repository click on the green "Code" button and choose "Download zip," making sure the repository is downloaded to the home directory on the data capsule which is `/home/dcuser` on all data caspules and is usually marked with a house icon. This is necessary because the code in the notebooks operate under the assumption the repository is in the home driectory. Once the .zip file is downloaded, extract it, making sure to keep the extracted folder in the home directory.

#### Further prep
Now that the repository is downloaded and extracted, the conda environment needs to be created. In addition to the notebooks and a folder for some data output, the repository contains an environment.yml file which is the anaconda environment necessary to run the notebooks on the HTRC data capsules. The environment contains all the Python Libraries necessary to run the notebooks. Creating the environment should not break the current Python setup on the data capsules. To use the environment.yml file to create the conda environment you will need to open the terminal and type or copy and paste the following"

`cd HTRC-JupyterNotebooks-main; conda env create -f environment.yml; cd ..; source activate nb_env; python -m spacy download en_core_web_sm; python -m spacy download zh_core_web_sm; python -m spacy download fr_core_news_sm; python -m spacy download de_core_news_sm; python -m spacy download it_core_news_sm; python -m spacy download ja_core_news_sm; python -m spacy download pt_core_news_sm; python -m spacy download ru_core_news_sm; python -m spacy download es_core_news_sm; python -m spacy download xx_ent_wiki_sm`

Much of this code will download and install the lemmatization piplines for the `spacy` python library. Once you have run this script in the command line, you should not need to run it again. Now you should be ready to use the Jupyter Notebooks provided in this repository.
