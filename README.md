# HTRC-JupyterNotebooks

#### Downloading this repository
This repository contains Jupyter Notebooks containing Python code that performs text analytics algorithms as well as detailed annotations and instructions for running the code. This repository and the accompanying conda environment come pre-installed on all HTRC data capsules. However, if you wish to download this repository somewhere other than a data capsule, click on the green "Code" button and choose "Download zip," making sure the repository is downloaded to the home directory of your operating system (macOS: `/Users/username` | Windows: `C:`). This is necessary because the code in the notebooks operate under the assumption the repository is in the home driectory. Once the .zip file is downloaded, extract it, making sure to keep the extracted folder in the home directory.

#### For use in HTRC Data Capsules
If you plan to use this notebook in an HTRC Data Capsule, you simply need to create and launch a Data Capsule and double click the icon on the desktop labeled `Launch-LSA-JupyterNotebook`. This will create the required Anaconda environment with all of the dependent Python libraries and their correct versions and also launch the Jupyter server on your Data Capsule. Note: your Data Capsule must be in secure mode to download data (which is the first task of the notebook.

#### For use out of HTRC Data Capsule
Now that the repository is downloaded and extracted, the conda environment needs to be created. In addition to the notebooks and a folder for some data output, the repository contains an environment.yml file which is the anaconda environment necessary to run the notebooks. The environment contains all the Python Libraries necessary to run the notebooks. Creating the environment should not break the current Python setup on your system. To use the environment.yml file to create the conda environment you will need to open the terminal (macOS) or cmd prompt (Windows) and type or copy and paste the following"

`cd HTRC-JupyterNotebooks-main; conda env create -f environment.yml; cd ..; source activate nb_env; python -m spacy download en_core_web_sm; python -m spacy download zh_core_web_sm; python -m spacy download fr_core_news_sm; python -m spacy download de_core_news_sm; python -m spacy download it_core_news_sm; python -m spacy download ja_core_news_sm; python -m spacy download pt_core_news_sm; python -m spacy download ru_core_news_sm; python -m spacy download es_core_news_sm; python -m spacy download xx_ent_wiki_sm`

This process can take as long as 15 minutes to complete. Much of this code will download and install the lemmatization piplines for the `spacy` python library. Once you have run this script in the command line, you should not need to run it again. Now you should be ready to use the Jupyter Notebooks provided in this repository.

#### Data Capsule Requirements
The notebooks work best on data capsules with 4 vcpus and 16 GB of ram. Data capsules with lower specs can and have run into memory usage issues when running the notebooks on larger datasets. In addition, the data capsules use Firefox as the default browser. Since Jupyter Notebooks use the browser to run, and Chrome has a higher allowable memory on the data capsules, it is also recommended that you switch your default browser from Firefox to Chrome. This can be done by clicking in the "Search your computer" icon in the top left corner of the data capsule and searching for Chrome. When you open Chrome a message stating that Chrome is not your default browser and asking if you want to make it your default browser should appear. Respond in the affirmative that you would like Chrome to be your default browser. If you have any issues with creating a data capsule with the necessary specs or changing the default browser you can contact the HathiTrust Research Center for assistance at htrc-help@hathitrust.org.
