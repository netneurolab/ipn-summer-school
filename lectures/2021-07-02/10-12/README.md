# Welcome to Dynamical Systems!


## * Resources:

Here we've compiled a set of interesting papers at the intersection of dynamical systems and neuroscience: 

* [](): **
* 


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
