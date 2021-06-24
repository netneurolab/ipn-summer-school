Welcome to the last lecture: Contextualizing Results!

# Set-up

At the start of the lecture, I'll ask everyone to do a little set-up.
You don't need to do this before the lecture, but if you'd like to, here's what we'll do.

## Using Google Collab
- click [here](https://drive.google.com/file/d/1huYhQz_KDZLTsy0e47-05jWWX71L2hFc/view?usp=sharing) to grab the file `schaefer200coords.npy` (brain region coordinates for the Schaefer 2018 200-node parcellation) and put it in your own Google Drive. 
- open a new collab notebook (just as you would open a new Google Doc)
- copy and paste the code block below and run it (approx 10 min). Don't close your collab notebook! This will be the notebook you use throughout the demos.
```
!pip install --upgrade numpy scipy matplotlib pandas
!pip install git+https://github.com/netneurolab/netneurotools
!pip install git+https://github.com/neurosynth/neurosynth
!pip install abagen

import abagen
from nilearn.datasets import fetch_atlas_schaefer_2018
import pandas as pd
import numpy as np
from scipy.spatial.distance import squareform, pdist
import matplotlib.pyplot as plt
from scipy.stats import zscore, pearsonr

# get atlas
schaefer = fetch_atlas_schaefer_2018(n_rois=200)

# get node x gene data for all 6 donors
# return_donors=False for full concatenated node x gene matrix
# this might take some time which is why we're running it early on
expression = abagen.get_expression_data(schaefer['maps'], return_donors=True)
```
- run [this](fetch_and_parcellate_neurosynth.ipyn) script (this will also take some time, approx 30 min)
- upload the downloaded output of `fetch_and_parcellate_neurosynth.ipyn` (called `atl-schaefer2018_res-200_neurosynth.csv`) into your Google Drive

## Using Python locally
- click [here](https://drive.google.com/file/d/1huYhQz_KDZLTsy0e47-05jWWX71L2hFc/view?usp=sharing) to grab the file `schaefer200coords.npy` (brain region coordinates for the Schaefer 2018 200-node parcellation) and put it somewhere you can find it (to `np.load('schaefer200coords.npy')` later on)
- make sure you've got all the dependencies as described [here](https://github.com/netneurolab/ipn-summer-school) under Installation > Python
- copy and paste this block of code into your editor and run it:
```
import abagen
from nilearn.datasets import fetch_atlas_schaefer_2018
import pandas as pd
import numpy as np
from scipy.spatial.distance import squareform, pdist
import matplotlib.pyplot as plt
from scipy.stats import zscore, pearsonr

# get atlas
schaefer = fetch_atlas_schaefer_2018(n_rois=200)

# get node x gene data for all 6 donors
# return_donors=False for full concatenated node x gene matrix
# this might take some time which is why we're running it early on
expression = abagen.get_expression_data(schaefer['maps'], return_donors=True)
```
- run [this](fetch_and_parcellate_neurosynth.py) script (this will take some time, about 10 min on my local device but it will depend on your device)

And that's it!
You should be good to go.
Again, you don't need to do this before lecture.

# Resources

I have compiled a list of resources (papers, handy GitHub repos, open-source data repos) that I reference during my lecture, in case you'd like to explore certain topics further.
I don't expect you to have read or familiarized yourself with any of these resources prior to the lecture.
The bullet points indicate the context from which I introduced (or briefly referenced) the paper/repo/dataset.

## Papers

- [Burt et al., 2018](https://www.nature.com/articles/s41593-018-0195-0): *Hierarchy of transcriptomic specialization across human cortex captured by structural neuroimaging topography*
  - linking genes to brain structure
- [Suarez et al., 2020](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-6613(20)30026-7): *Linking structure and function in macroscale brain networks*
  - review article
  - linking structure and function
- [Vasquez-Rodriguez et al., 2019](https://www.pnas.org/content/116/42/21219): *Gradients of structure-function tethering across neocortex*
  - structure-function coupling
  - also includes one of the spin-test methods
- [Seidlitz et al., 2020](https://www.nature.com/articles/s41467-020-17051-5): *Transcriptomic and cellular decoding of regional brain vulnerability to neurogenetic disorders*
  - cell type deconvolution
- [Zhu et al., 2018](https://www.cell.com/neuron/pdf/S0896-6273(18)30581-6.pdf): *Architecture of the Mouse Brain Synaptome*
  - linking synapses and brain structure
- [Cizeron et al., 2020](https://science.sciencemag.org/content/369/6501/270.abstract): *A brainwide atlas of synapses across the mouse life span*
  - linking synapses and brain structure
- [Zilles & Palomero-Gallagher, 2017](https://www.frontiersin.org/articles/10.3389/fnana.2017.00078/full): *Multiple transmitter receptors in regions and layers of the human cerebral cortex*
  - neurotransmitter receptor distributions
  - data openly availble in supplementary tables!
- [Zilles et al., 2015](https://www.sciencedirect.com/science/article/pii/S0010945214002287): *Common molecular basis of the sentence comprehension network revealed by neurotransmitter receptor fingerprints*
  - linking receptors and brain function
- [Beliveau et al., 2017](https://www.jneurosci.org/content/37/1/120): *A high-resolution in vivo atlas of the human brain's serotonin system*
  - includes PET serotonin receptor maps
- [Nørgaard et al., 2021](https://www.sciencedirect.com/science/article/pii/S1053811921001555): *A high-resolution in vivo atlas of the human brain's benzodiazepine binding site of GABA<sub>A</sub> receptors*
  - includes available GABA density maps
- [Hansen et al., 2021](https://github.com/netneurolab/hansen_genescognition/blob/master/hansen2021nathumbehav.pdf): *Mapping gene transcription and neurocognition across human neocortex*
  - linking genes to cognition
  - uses spin-tests, gene set enrichment analysis, cell-type deconvolution
  - several figures in the lecture come from here
  - yeah, self-promotion I guess
- [Yeo & Krienen et al., 2011](https://journals.physiology.org/doi/full/10.1152/jn.00338.2011): *The organiation of the human cerebral cortex estimated by intrinsic functional connectivity*
  - resting-state network definition
- [Vertes et al., 2016](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2015.0362): *Gene transcription profiles associated with inter-modular hubs and connection distance in human functional magnetic resonance imaging networks*
  - mapping of Von Economo cytoarchitectonic classes (originally defined by Von Economo & Konskinas)
- [Paquola et al., 2019](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3000284): *Microstructural and functional gradients are increasingly dissociated in transmodal cortices*
  - mapping of Mesulam levels of laminar differentiation (originally defined by Mesulam himself)
- [Hawrylycz et al., 2012](https://www.nature.com/articles/nature11405): *An anatomically comprehensive atlas of teh adult human brain transcriptome*
  - original AHBA paper
- [Arnatkeviciute et al., 2019](https://www.sciencedirect.com/science/article/pii/S1053811919300114): *A practical guide to linking brain-wide gene expression and neuroimaging data*
  - AHBA data processing
- [Yarkoni et al., 2011](https://www.nature.com/articles/nmeth.1635): *Large-scale automated synthesis of human functional neuroimaging data*
  - original Neurosynth paper
- [Fornito et al., 2019](https://www.sciencedirect.com/science/article/pii/S1364661318302535): *Bridging the gap between connectome and transcriptome*
  - review article 
  - includes gene coexpression vs distance
- [Shafiei et al., 2020](https://elifesciences.org/articles/62116): *Topographic gradients of intrinsic dynamics across neocortex*
  - temporal similarity vs distance
- [Alexander-Bloch et al., 2018](https://www.sciencedirect.com/science/article/pii/S1053811918304968): *On testing for spatial correspondence between maps of human brain structure and function*
  - original spin test paper
- [Markello & Misic, 2021](https://www.sciencedirect.com/science/article/pii/S1053811921003293): *Comparing spatial null models for brain maps*
  - comparing spatial null models (and I used many figures from here)
- [Fulcher et al., 2021](https://www.nature.com/articles/s41467-021-22862-1): *Overcoming false-positive gene-category enrichment in the analysis of spatially resolved transcriptomic brain atlas data*
  - Gene set enrichment analysis the Right Way

## GitHub Repos

- [abagen](https://github.com/rmarkello/abagen): processing AHBA data
- [cell-type deconvolution](https://github.com/jms290/PolySyn_MSNs): includes `celltypes_PSP.csv`
- [hansen_genescognition](https://github.com/netneurolab/hansen_genescognition): data and code for [Hansen et al., 2021](https://github.com/netneurolab/hansen_genescognition/blob/master/hansen2021nathumbehav.pdf), including cell type deconvolution, gene ontolgoy, spin-tests, PLS, Neurosynth, and AHBA usage
- [neurosynth](https://github.com/neurosynth/neurosynth): Neurosynth code
- [netneurotools](https://github.com/netneurolab/netneurotools): includes spin test code, but also a LOT more
- [markello_spatialnulls](https://github.com/netneurolab/markello_spatialnulls): data and code for [Markello & Misic, 2021](https://www.sciencedirect.com/science/article/pii/S1053811921003293) which includes everything you need to do all types of spin tests
- [GeneCategoryEnrichmentAnalysis](https://github.com/benfulcher/GeneCategoryEnrichmentAnalysis): Matlab package for finding gene set enrichments using spatial null models


## Open-source data sources

- [The Allen Human Brain Atlas](https://human.brain-map.org/): microarray gene expression data in the human brain
- [BrainSpan](https://www.brainspan.org/): microarray gene expression data in the human brain across the lifespan (from fetus to adult)
- [Neurobiology Research Unit](https://xtra.nru.dk/index.html): [serotonin](https://xtra.nru.dk/FS5ht-atlas/) and [GABA](https://xtra.nru.dk/BZR-atlas/) PET density data
- [Human Connectome Project](https://db.humanconnectome.org/app/template/Login.vm): structural, functional, and behavioural data for many humans (needs login info)
- [Neurosynth](https://neurosynth.org): meta-analytic functional association maps
- [UK Biobank](https://www.ukbiobank.ac.uk/): Demographic and behavioural data on many humans
