# Graph Theory

## Resources:
Here's a list of useful resources:

### Coding resources:
* [BCT (Matlab)](https://sites.google.com/site/bctnet/): Brain Connectivity Toolbox which contains useful functions for brain networks analysis.
* [BCT (Python)](https://github.com/aestrivex/bctpy): Brain Connectivity Toolbox for Python.
* [netneurotools](https://netneurotools.readthedocs.io/en/latest/): Tools for network neuroscience.
* [NetworkX](https://networkx.org/): Python package for network analysis.

### Papers:
* [Hagmann et al. (2008) PLoS Biology](https://doi.org/10.1371/journal.pbio.0060159): *Mapping the Structural Core of Human Cerebral Cortex*
* [Bullmore & Sporns (2009) Nature reviews neuroscience](https://doi.org/10.1038/nrn2575): *Complex brain networks: graph theoretical analysis of structural and functional systems*
* [Rubinov & Sporns (2010) NeuroImage](https://doi.org/10.1016/j.neuroimage.2009.10.003): *Complex network measures of brain connectivity: Uses and interpretations*
* [van den heuvel & Sporns (2011) Journal of Neuroscience](https://doi.org/10.1523/JNEUROSCI.3539-11.2011): *Rich-Club Organization of the Human Connectome*
* [Sporns & Betzel (2016) Annual Review of Psychology](https://doi.org/10.1146/annurev-psych-122414-033634): *Modular brain networks*

### Book:
* [Fundamentals of Brain Network Analysis](https://www.sciencedirect.com/book/9780124079083/fundamentals-of-brain-network-analysis)
* [Networks](https://global.oup.com/academic/product/networks-9780198805090?cc=ca&lang=en&)
* [Networks of the brain](https://mitpress.mit.edu/books/networks-brain)
* [Network Science](http://networksciencebook.com/)

Those books should be freely available online via the [McGill Library](https://www.mcgill.ca/library/). The Network Science book is freely available, directly from the website.

## The lecture:

The lecture will consist in a theory section and a tutorial section.

### Theory:
The content covered in this lecture will be:

* What is graph theory?
* How do we reconstruct a brain network?
* What are the common measures used in graph theory?
* What has graph theory told us about the brain?
* What are the exciting new avenues in network neuroscience?

### Tutorial:
For the tutorial section of the lecture, you will have two different options:

#### Option A: Google Colab Notebook

You can follow the tutorial with Google Colab. The notebook is available here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vincebaz/ipn-summer-school/blob/main/lectures/2021-06-30/10-12/graph_theory_tutorial_colab.ipynb)

##### Requirements/Steps:

1. You will first need a Google Account.
2. You must download the numpy files containing the data that will be used during the demo. Namely:
    * coords.npy
    * FC.npy
    * SC.npy
3. From your Google Drive home directory, you must store these files in a a folder named "IPN Summer School".

#### Option B: Jupyter Notebook

You can follow the tutorial using the Jupyter notebook available [here](https://github.com/VinceBaz/ipn-summer-school/blob/main/lectures/2021-06-30/10-12/graph_theory_tutorial_local.ipynb).

##### Requirements/Steps:

1. You will need Python and a local Python environment.

    If you are unfamiliar with Python, I highly recommend installing [Anaconda](https://www.anaconda.com/). The basic installation package will give you a large number of tools that are useful for data science. Anaconda should create for you a python environment will a large number of useful python packages already installed. Among them are [Jupyter Notebook](https://jupyter.org/index.html) which will be used to visualize the Notebook, and [Spyder](https://www.spyder-ide.org/) which is a nice IDE that I recommend.

If you are using Windows and downloaded Anacondqa, you should now have access to an "Anaconda Prompt" (via the Start Menu). The next steps (i.e. installing the python packages that we will use) should be done using the Anaconda Prompt (and not the normal cmd prompt).

2. If you chose to use the (base) conda environement, you can immediately skip to Step 3. Alternatively, you might want to create an additional Conda virtual environement for this tutorial. To do so, please follow  [the steps presented by Estefany for her machine learning course](https://github.com/netneurolab/ipn-summer-school/tree/main/lectures/2021-06-29/13-15).

3. You will need to install the netneurotools and bct packages using:

```
pip install git+https://github.com/aestrivex/bctpy
pip install git+https://github.com/netneurolab/netneurotools
```

4. You will then need to download the files in the data folder as well as the Jupyter Notebook and store them in any folder that you prefer (they must be in the same folder).

5. You can then open Jupyter-notebook by typing in the terminal:

```
jupyter-notebook
```
