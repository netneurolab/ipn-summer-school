# Advanced Analytics for Neuroscience (Summer 2021)

Welcome to Advanced Analytics for Neuroscience, part of the IPN Summer School 2021 program!

We're excited to take a deep dive into a bunch of really exciting topics over the course of the week.
This repository contains all of the course materials, instructions, slides, and other miscellany that we'll be using throughout the week.
It's liable to be modified / changed as the course progresses, so be sure to check back here frequently for updates!

## Schedule

Date | Time | Topic | Instructor | Materials
--- | --- | --- | --- | ---
28 June | 9-10h | Analytics for neuroscience | B Misic | [Link](./lectures/2021-06-28/09-10)
28 June | 10-12h | Data science | R Markello | [Link](./lectures/2021-06-28/10-12)
28 June | 13-15h | Dimensionality reduction | Z-Q Liu | [Link](./lectures/2021-06-28/13-15)
29 June | 10-12h | Multivariate associative techniques | B Misic | [Link](./lectures/2021-06-29/10-12)
29 June | 13-15h | Machine learning | E Suarez | [Link](./lectures/2021-06-29/13-15)
30 June | 10-12h | Graph theory | V Bazinet | [Link](./lectures/2021-06-30/10-12)
30 June | 13-15h | Time series analyis | G Shafiei | [Link](./lectures/2021-06-30/13-15)
1 July | &mdash; | Happy Canada Day! :canada: :maple_leaf: | &mdash; | &mdash;
2 July | 10-12h | Dynamical systems | E Suarez | [Link](./lectures/2021-07-02/10-12)
2 July | 13-15h | Contextualizing results | J Hansen | [Link](./lectures/2021-07-02/13-15)

## Background / assumptions

While the course materials themselves are relatively agnostic to programming language, most of the hands-on tutorials will demonstrate applications using Python packages.
As such, the instructors will assume some modicum of familiarity with Python.
(If you are not familiar with Python that is totally okay&mdash;you will still be able to gain a lot from the course, and the tutorials are designed such that you don't *need* to code along yourself in order to learn / benefit from them.)

## Installation

In order to get the best experience from this course it is recommended you install the following software packages.
(Note that you will still be able to follow along with the materials if you do not have these installed, but you will not be able to reproduce the tutorials and demonstrations yourself.)

1. [git](https://git-scm.com/downloads)
1. Matlab (though you can opt to use [Matlab online](https://www.mathworks.com/academia/tah-portal/mcgill-university-30521249.html) if you would prefer not to install this locally)

Also, it is recommended you create a [GitHub account](https://github.com/signup) if you do not already have one.
(If you have one make sure you know your password!)

### Python

While many of the tutorials will use Python, we intend to use [Google Colab](https://colab.research.google.com/) notebooks for the majority of these demonstrations which means *you shouldn't need to install anything locally*.
However, if you would prefer to run everything on your local computer you will need to install Python and all the required Python dependencies.

#### Miniconda

We recommend using [miniconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html) to get Python up and running on your computer.
Miniconda is a (primarily Python) environment manager that handles installing and managing (Python) packages and dependencies in a really seamless manner.
Once you have miniconda installed and working on your computer you can create a new Python environment with all the required Python dependencies by downloading the [`environment.yml`](./environment.yml) file from this repository and running:

```bash
conda env create -f environment.yml
```

You can then activate this environment by opening a terminal and typing:

```bash
conda activate nnlabsummer
```

#### Pip

If you have Python installed via some other mechanism you can use `pip` to install all the dependencies by downloading the [`requirements.txt`](./requirements.txt) file from this repository and running:

```bash
pip install -r requirements.txt
```

## Questions? Comments? Concerns?

If you've made a GitHub account (see [Installation](#installation)), you can [open an issue](https://github.com/netneurolab/ipn-summer-school/issues/new) on this repository and one of the instructors will get back to you asap!
If you would prefer to discuss something privately you can e-mail the course advisor ([B Misic](https://netneurolab.github.io/team/)) directly.
