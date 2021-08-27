# python_setup

This repository is to help new users set up python quickly and provide the environment to run my python scripts/notebooks. For the speediest set-up just follow the items in **bold** font.

## 1. Install Anaconda (or Pip, but Anaconda will get you going faster)

Anaconda installers can be obtained at https://www.anaconda.com/products/individual, and pip can be obtained using a package manager such as “apt-get pip”. I recommend using Miniconda (**https://docs.conda.io/en/latest/miniconda.html**), because it is a minimal installation, and one can then install my environment library set that I provide on top of it (see Step 2).Pip is commonly used on Linux/OSX for installing Python libraries. Anaconda is used on Windows, but also works fine on Linux and OSX. Anaconda also has some quality of life benefits (but also some drawbacks) over pip. But I still suggest you go for Anaconda first to get started more easily. 

## 2. Install my libraries (aka, environment)
First, use my library configuration file cf2.yml, also known as an environment Anaconda, to re-create my environment:

**conda env create -f cf2.yml**

Launch the (Anaconda) prompt. On Linux you would type something like: 
conda activate cf2 (on windows it is just “**activate cf2**”)

Change directory to where the .ipynb file is stored. Then put **jupyter lab** in the prompt. A browser will open. On the left hand side is a navigation panel, and you can open the .ipynb file. The main panel will then show different cells, and you can step through each of them using the play button. Edit as needed. The notebook is good for prototyping. One can also save this as a .py script and just run directly. 

## 3. Reference
https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

## 4. Other notes
- To install any other libraries I don’t use, you can do so with "conda install <library>". 
- To export your own set of libraries as .yml to share with others, you can do so via "conda env export > environment.yml"
- To make your own environment – this may be necessary to run certain libraries that have a fairly unique set of requirements/dependencies, you can do so with “conda create –name <envnamehere>”
- I strongly recommend to set the default channel from which to obtain libraries/updates to be conda-forge. This can be done via "conda config --add channels conda-forge"

This last recommendation stems from the conda-forge repository being very large (having many versions of many libraries) and also being frequently updated. Thus, one is most likely to find the best compatibility between the various libraries when using this channel. A important problem and source of headaches is that when libraries are installed from different repositories, while the libraries may look like they installed okay, they may not actually play nice with one another.

to install specific version of a library, "conda install pandas=0.24.2"
to create a new environment having a particular version of library, "conda create -n tstenv pandas=0.24.2"
