Replication code for the paper "Mining Brand Perceptions from Twitter Social Networks," by Aron Culotta and Jennifer Cutler, published in *Marketing Science*.


## Data

All requisite data is downloadable here (333M):

<https://www.dropbox.com/s/rvzn98l3a3278v9/mksci-data.tgz?dl=1>

The contents of this archive are as follows: 
- **brands.txt**: A list of Twitter accounts for each of the 168 brands considered (after removing those without sufficient survey responses).
- **brands_followers.txt**: The follower ids for each brand, up to 500K. All follower files have one account per line. The first value is the time stamp for when the followers were collected, the second value is the screen_name of the account, the remaining values are the Twitter IDs of each follower.
- **brand_followers_unfiltered.txt**: The follower ids for each brand from the original 231 brands prior to filtering.

Subfolders contain information for each perceptual attribute:

- **eco**: Environmental friendliness attribute.
- **luxury**: Luxury attribute.
- **nutrition**: Nutrition attribute.
- **eco-nonprofit:** Same as **eco**, but uses manually collected exemplars from Charity Navigator (for Table 3).

Each of these subfolders contains the following:

- **default/**: A subfolder with the predicted ratings according to each of the 12 algorithm variants described in the paper (c.f. Table 4).
- **diagnose/**: A subfolder with the correlation between survey and prediction using a single exemplar at a time (for Figure 9).
- **exemplars.txt**: The exemplar Twitter accounts for this perceptual attribute.
- **exemplar_followers.txt**: The followers of each exemplar.
- **nexemplars/**: Results of correlation versus number of exemplars (Figure 7a)
- **survey/**: A subfolder with the average survey ratings for this perceptrual attribute, separated by brand category (e.g., Cars, Apparel, ...)


## Code

All analysis is done in Python, using a single iPython notebook:
**[MKSCI-Replication.ipynb](https://github.com/tapilab/mksci-2015-brand-perceptions/blob/master/Mksci-Replication.ipynb):** 

The IPython notebook replicates the figures and tables from the paper. To learn more about iPython Notebooks, see the documentation here: <http://ipython.org/notebook.html>. Notebooks are increasingly being used for replicability, as the notebook integrates Python code, its output, and documentation in one file (for an overview, see http://www.nature.com/news/interactive-notebooks-sharing-the-code-1.16261). 

It can take some effort to get iPython installed locally. If this is an issue, a static version of the notebook can be viewed here:
<Mksci-Replication.html>

Additionally, we have integrated our code with Binder (http://mybinder.org/), which is a pretty amazing tool that provides a web interface to run iPython notebooks on a remote server. This allows one to reproduce our analysis without installing or configuring anything. This is now available here:
<http://mybinder.org/repo/tapilab/mksci-2015-brand-perceptions>


[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/tapilab/mksci-2015-brand-perceptions)

