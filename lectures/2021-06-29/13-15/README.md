# Welcome to intro to machine-learning for neuroscience!


## Resources:


## Hands-on tutorial requirements:
### Using Google Collab
If you do not want to install anything you can use google collab to run the demo. All you will need is a Google account. Just click [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-06-29/13-15/demo.ipynb) to open the notebook. 

Else, if you do not want to get your hands dirty, and just want to passively follow the demo, you can visualize the notebook by clicking [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/netneurolab/ipn-summer-school/blob/main/lectures/2021-06-29/13-15/demo.ipynb?flush_cache=true)

### Using Python locally
Alternatively, you can also run the Jupyter notebook locally in your own computer:

1. Install  [Anaconda](https://www.anaconda.com/products/individual).
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
    
4. Install Nilearn
    ```
    pip install nilearn
    ```
    
 5.  Open the Jupyter-notebook:
     ```
     jupyter-notebook
     ```
     
You’re ready to go! 

NOTE: the name **ipn_summer_school** can be replaced by anything you want, hopefully a short and meaningful name that tells you what the environment is about.
This same environment will be used for the hands-on dynamical systems tutorial.
