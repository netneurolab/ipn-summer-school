# Intro to Machine-Learning for neuroscience

## Requirements for the Machine-learning hands-on tutorial:
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
