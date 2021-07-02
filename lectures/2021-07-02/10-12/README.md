# Welcome to Dynamical Systems!


## * Resources:

Here we've compiled a set of interesting papers at the intersection of dynamical systems and neuroscience: 

Computational Neuroscience:
* [Rabinovich et al., 2006](https://journals.aps.org/rmp/abstract/10.1103/RevModPhys.78.1213): *Dynamical principles in Neuroscience*
* [Rabinovich et al., 2012](https://mitpress.mit.edu/books/principles-brain-dynamics): *Principles of Brain Dynamics: Global State Interactions (Computational Neuroscience Series)* - BOOK
* [Rabinovich et al., 2012](https://www.sciencedirect.com/science/article/pii/S1571064511001448): *Information flow dynamics in the brain*
* [Cocchi et al., 2017](https://www.sciencedirect.com/science/article/pii/S0301008216301630): *Criticality in the brain: A synthesis of neurobiology, models and cognition*
* [Buonomano and Maass, 2009](https://www.nature.com/articles/nrn2558): *State-dependent computations: spatiotemporal processing in cortical networks*
* [Beggs, 2007](https://royalsocietypublishing.org/doi/pdf/10.1098/rsta.2007.2092): *The criticality hypothesis: how local cortical networks might optimize information processing*
* [Sussillo, 2014](http://www.rctn.org/vs265/sussillo-dynamical-systems-curropin.pdf): *Neural circuits as computational dynamical systems*
* [Vyas, et al., 2020](https://www.annualreviews.org/doi/abs/10.1146/annurev-neuro-092619-094115): *Computation Through Neural Population Dynamics* 
* [Sussillo and Barak, 2013](https://web.stanford.edu/class/cs379c/archive/2016/calendar_invited_talks/articles/SussilloandBarakNC-13.pdf): *Opening the Black Box: Low-Dimensional Dynamics in High-Dimensional Recurrent Neural Networks*
* [Mastrogiuseppe and Ostojic, 2018](https://www.sciencedirect.com/science/article/pii/S0896627318305439): *Linking Connectivity, Dynamics, and Computations in Low-Rank Recurrent Neural Networks*

Some researches dedicated to the study of brain dynamics are:
* [Mikhail I. Rabinovich](https://scholar.google.com/citations?user=zplPdX4AAAAJ&hl=en) - Theoretical/Computational neuroscience
* [Pablo Varona](https://scholar.google.ca/citations?user=JrMlehIAAAAJ&hl=en)- Theoretical/Computational neuroscience
* [Gustavo Decco](https://scholar.google.es/citations?user=xMh3uN8AAAAJ&hl=en)- Theoretical/Computational neuroscience
* [Michael Breakspear](https://scholar.google.com/citations?user=hrx691cAAAAJ&hl=en)- Theoretical/Computational neuroscience
* [Viktor Jirsa](https://scholar.google.ca/citations?user=0ZVdLpMAAAAJ&hl=en)- Theoretical/Computational neuroscience
* [David Sussillo](https://scholar.google.com/citations?user=ebBgMSkAAAAJ&hl=en)- Computational neuroscience + AI (recurrent neural networks)
* [Steven Strogatz](http://www.stevenstrogatz.com) - Nonlinear dynamics and complex systems

And these are just a few of them!!!

## * Hands-on tutorial requirements:
### Using Google Collab
If you do not want to install anything locally, you can use Google Collab to run the demos. To do so you will need a Google account. To open and run a notebook just click on the corresponding link: 
* Demo1: A simple 3D Linear Dynamical System: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-07-02/10-12/demo1.ipynb)

* Demo2: Stability of 2D Linear Systems: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-07-02/10-12/demo2.ipynb)

* Demo3: Stability of Nonlinear Systems: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-07-02/10-12/demo3.ipynb)

* Demo4: The Morris-Lecar model + Bifurcation Analysis: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-07-02/10-12/demo4.ipynb)

### Using Python locally
Alternatively, you can also run things locally in your own computer. This requires some extra installation steps:

1. Install  [Anaconda](https://www.anaconda.com/products/individual)
2. Create a [Conda virtual environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands). To do so, open the terminal and type:
    
    ```
    conda create --name ipn_summer_school python=3.6 numpy scipy pandas scikit-learn nilearn seaborn matplotlib
    conda activate ipn_summer_school
    ```
    
3. Install Jupyter and add your new conda environment to the kernels available:
    
    ```
    conda install jupyter 
    conda install -c anaconda ipykernel
    python -m ipykernel install --user --name=machine-learning
    ```
    
 5. Download the **demoX.ipynb** files found in this repo, and place them into a new directory in your local computer.

 6. In the terminal, navigate to the directory where you placed the files:
 
     ```
     cd /path/to/directory
     ```
 
 7.  Open Jupyter-notebook by typing in the terminal:
     
     ```
     jupyter-notebook
     ```
 8. Click on the **demoX.ipynb** file. 
 
You’re ready to go! 

NOTE: the name **ipn_summer_school** can be replaced by anything you want, hopefully a short and meaningful name that tells you what the environment is about.
This same environment will be used for the hands-on dynamical systems tutorial.
