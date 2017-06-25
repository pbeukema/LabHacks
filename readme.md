### Advice on...

[Analysis](#analysis)   
[Programming](#programming)   
[Generating figures](#generating-publication-quality-figures)    
[Statistics](#statistical-analysis)      
[fMRI](#doing-fmri)  
[Literature search](#literature-search)  
[Writing papers](#writing-papers)   
[Meetings](#meetings-with-your-pi)     
[Meta Neuro Papers](#Papers)
##
## Analysis 
* Start with a clear and universal directory structure for organizing your analysis, data, figures, etc. [Here](http://nikola.me/folder_structure.html) is a template you can follow for a transparent directory structure.  

* [Atom](https://atom.io/) is very powerful and free text editor that integrates seamlessly with github. 
Use it for writing experimental code, scanner code, bash scripts and so on. 
(Hint: Run scripts from atom with package "script")

* Use [jupyter notebooks](http://jupyter.readthedocs.io/en/latest/index.html) for development and for analysis pipelines. Install [Kyle Dunovan's](https://github.com/dunovank) [jupyter themes](https://github.com/dunovank/jupyter-themes) to make your notebooks pretty and work faster. 

* Make an "autopilot" script for your analyses, so that figures (and even posters if you are feeling ambitious) are updated in real time while the data is collected. Write a [cron job](http://www.adminschoice.com/crontab-quick-reference) to execute an autopilot script that integrates newly collected data and updates analyses perhaps with an email summarizing the results sent to you or your advisor. You can find some autopilot examples [here](https://github.com/pbeukema/rsaRemap/blob/master/modmap_autopilot.py). 

* Make a startup file for your jupyter notebooks that preloads modules like numpy and scipy to save you time and also so that your figures are always publication quality, from the get go, without modification. The config file can specify font sizes, legends, color themes etc.

* [Here](https://unsupervisedmethods.com/cheat-sheet-of-machine-learning-and-python-and-math-cheat-sheets-a4afe4e791b6) is an extremely well curated series of quick references for data science in python (numpy, scipy, pandas), ML algorithms, probability and more 
##  Programming 
* Start using github. It is excellent for version control and for sharing (instead of having analysis_v4_p3.2_final.py you just have analysis.py). Other researchers can replicate exactly what you did. This will save you time, if someone emails you for example. 

* You or your lab may be most familiar with Matlab. It is worth considering a switch to [Python](https://www.python.org/). Python offers simpler syntax, enables system wide interfacing, is open source, free and for these reasons is being used by more and more scientists. Replication is far easier with Python than Matlab. 

* [Learn Python the Hard Way](https://learnpythonthehardway.org/book/) is a tutorial for learning python. It consists of 52 exercises from installing Python (Exercise 0) to building a web game (Exercise 52). Everyone in our lab who learned python used this tutorial.

* Need to sync files across your various lab computers/clusters and laptop you use at home and don't want to use Dropbox? Use [rsync](https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-on-a-vps) instead. e.g:
```bash
rsync -zavr -e ssh --delete --include '*/' --include='*include_these_files.[ext]' --exclude='*' [local_dir] [remote_server]:[remote_dir]
```

* Thomas Wiecki provides a [great introduction](http://nbviewer.jupyter.org/format/slides/github/twiecki/pydata_ninja/blob/master/PyData%20Ninja.ipynb#/) to becoming a python data ninja.

* [Anaconda](https://www.continuum.io/downloads) provides a scientific distribution of python that enables high performance computing and analysis. 

* Become a pro at [bash shortcuts](https://ss64.com/bash/syntax-keyboard.html)- it will seriously save you a lot of time. 

* Simulate data and make sure that your analysis works the way you think that it is working. 

* Use hotkeys for [google](https://support.google.com/chrome/answer/157179?hl=en), [gmail](https://support.google.com/mail/answer/6594?co=GENIE.Platform%3DDesktop&hl=en), [atom](https://github.com/nwinkler/atom-keyboard-shortcuts), & [jupyter notebooks](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/). Consider a mechanical keyboard so your labmates love you, then hotkey some more. 

* Not sure how to code something? It may have an answer on [stack overflow](https://stackoverflow.com/). 

* Access anything or anywhere on your computer with minimal effort using Keyboard launchers like [Albert](https://github.com/albertlauncher/albert) for linux and [Alfred](https://www.alfredapp.com/) for mac. 

##  Generating Publication Quality Figures
* It is best to use whatever software you are using to get the figure as close to final as possible. Sometimes it is necessary to do some post edits in illustrator/inkscape but with diligent coding, you can usually avoid this, which will ultimately save you time. 

* For data visualization, [matplotlib](https://matplotlib.org) in python and a library called [seaborn](http://seaborn.pydata.org/index.html) are very useful tools to generate publication quality figures.

* Save your figures in svg, or eps. pngs do not scale well.
##  Statistical Analysis
* Learn to love Bayesian statistics, if you don't already.
[This](http://jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/) is an introduction on bayesian vs. frequentism written by [Jake Vanderplas](https://staff.washington.edu/jakevdp/), an astrophysicist and python developer. 


* Beware of p-values and null hypothesis significance testing in general. Read [this](http://ejwagenmakers.com/2007/pValueProblems.pdf) paper for some of the problems with p-values if you are not familiar with the controversy. [Here](http://www.stat.columbia.edu/~gelman/research/published/pvalues3.pdf) and [here](http://www.stat.columbia.edu/~gelman/research/published/retropower20.pdf) Andrew Gelman sheds light on ways to proceed. 

* As soon as possible, understand [bootstraping](https://en.wikipedia.org/wiki/Bootstrapping_(statistics)), [cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) and [permutation tests](https://en.wikipedia.org/wiki/Resampling_(statistics)). [Here](https://docs.google.com/presentation/d/11TozBxAaON1eFXeL6aK1USLtJyAbUaHhskcPkI0FLbc/edit#slide=id.g138cbbed1a_0_0 ) are some lecture notes that look at these topics in the context of multivariate pattern analysis in fMRI. 

* [Rob Kass](http://www.stat.cmu.edu/~kass/), CMU statistics faculty, has written [Ten Simple Rules for Effective Statistical Practice](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004961). They are extremely useful. 

* Are you still not using hierarchical Bayes? Everything is a trivial case of hierarchical Bayesian inference. Thomas Wiecki will show you the [way](http://twiecki.github.io/blog/2017/02/08/bayesian-hierchical-non-centered/). 

* Frequent [datatau](http://www.datatau.com/) for interesting news on data analysis

* Your stats question may have an answer over [here](https://stats.stackexchange.com/) on cross-validated

  ###  Statistics blogs
  * [While my MCMC gently samples](http://twiecki.github.io/)

  * [Pythonic perambulations](http://jakevdp.github.io/)

  * [Statistical Modeling, Causal Inference, and Social Science](http://andrewgelman.com/) 

##  Writing Papers
* See these [Ten simple rules for structuring papers](http://biorxiv.org/content/biorxiv/early/2016/11/28/088278.full.pdf
), written by [Konrad Kording](http://koerding.com/) and Brett Mensh. 

* Share your work with your friends as well as your enemies, the latter might give you even better criticism.

* Steven Pinker has some interesting thoughts on how to make academic writing [better](http://stevenpinker.com/files/pinker/files/why_academics_stink_at_writing.pdf)
##  Doing fMRI
* Organize your dataset using the [BIDS format](http://bids.neuroimaging.io/) - this will make your data more accessible to both your collaborators and the field at large. 

* If you can not write down the general linear model you are using from scratch and solve it in closed form, [learn how](http://www.brainvoyager.com/bvqx/doc/UsersGuide/StatisticalAnalysis/TheGeneralLinearModel.html).  

* [PyCortex](https://github.com/gallantlab/pycortex) provides excellent visualization of your statistical maps projected on the surface and dynamically generated in your browser. 
##  Literature Search
* Before you start down some major project that you will be committed to for years, understand the current literature in your topic. Understand very clearly why you are going to do what you are going to do. 

* Find articles before they are officially published on [arxiv](http://biorxiv.org/)

* You can search the literature with [Pubmed](https://www.ncbi.nlm.nih.gov/pubmed/) & [Google-scholar](https://scholar.google.com)

* You will need a citation manager early on, [PaperPile](https://paperpile.com) is a good one that is well integrated with Pubmed 

## Twitter is a great resource for identifying new papers, events, tips etc. 
* [@tdverstynen](https://twitter.com/tdverstynen)  cognitive neuroscience, imaging (DSI/fMRI)
* [@KordingLab](https://twitter.com/kordinglab)  neural data science, computational modeling, 
* [@StatModeling](https://twitter.com/StatModeling)  statistics, hierarhical bayesian modeling, R
* [@Neuro_Skeptic](https://twitter.com/Neuro_Skeptic)  neuroscience in general
* [@NKriegeskorte](https://twitter.com/NKriegeskorte)  fMRI, RSA, deep learning
* [@jakevdp](https://twitter.com/jakevdp)  python, data analysis, astrophysics
* [@fonnesbeck](https://twitter.com/fonnesbeck) statistical analysis in python

## Papers
* [Neuroscience Needs Behavior](http://www.cell.com/neuron/pdf/S0896-6273(16)31040-6.pdf)
* [Could a Neuroscientist Understand a Microprocessor](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005268)
##  Meetings 
* Never show up empty handed to meetings with your PI.
* Have a clear objective to all meetings that everyone else knows as well.
* Be able to show some evidence of your productivity. 

* You will have some days or weeks where nothing worked. I found that in those cases it is productive to have a "rainy day" folder containing interesting analyses/figures you have not yet shown. 
