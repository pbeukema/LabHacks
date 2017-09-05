

* [Data Analysis](#data-analysis)   
* [Programming](#programming)   
* [Making figures nice](#generating-publication-quality-figures)    
* [Statistics](#statistical-analysis)      
* [fMRI](#doing-fmri)  
* [Ephys](#analyzing-ephys-data)  
* [Biophysical modeling](#biophysical-and-molecular-modeling)
* [Lit search](#literature-search)  
* [Writing papers](#writing-papers)   
* [Grant Writing](#grant-writing)  
* [Meetings](#meetings-with-your-pi)     
* [Meta Neuro Papers](#papers)  
* [Survival Guides](#survival-guides)

##
All software links on this page are open source, and all other resources are free.

## Data Analysis
* Start every new research project with a clear and universal directory structure for organizing your analysis, data and figures. [Here](http://nikola.me/folder_structure.html) is a template as an example you can follow for a transparent directory structure.  

* Download [Atom](https://atom.io/). It is a very powerful and free! editor that integrates nicely with github.
Use it for writing text, markup, code, code, scripts, etc.

* Use [jupyter notebooks](http://jupyter.readthedocs.io/en/latest/index.html) for development and for analysis pipelines. Install [Kyle Dunovan's](https://github.com/dunovank) [jupyter themes](https://github.com/dunovank/jupyter-themes) to make your notebooks pretty and work faster.

* Consider [version-controlling your data](https://dataversioncontrol.com/) along with your [code](https://github.com). 

* Make an "autopilot" script for your analyses, so that figures (and even posters if you are feeling ambitious) are updated in real time while the data is collected. Write a [cron job](https://healthchecks.io/docs/cron/) to execute an autopilot script that integrates newly collected data and updates analyses perhaps with an email summarizing the results sent to you or your advisor. You can find some autopilot examples [here](https://github.com/pbeukema/rsaRemap/blob/master/modmap_autopilot.py).

* Make a startup file for your jupyter notebooks that preloads modules like numpy and scipy to save you time and also so that your figures are always publication quality, from the get go, without modification. The config file can specify font sizes, legends, color themes etc.

* Learning data science? [Here](https://unsupervisedmethods.com/cheat-sheet-of-machine-learning-and-python-and-math-cheat-sheets-a4afe4e791b6) is an extremely well curated series of quick references for data science in python (numpy, scipy, pandas), ML algorithms, probability and more

* Diving into deep learning? [Here](https://startupsventurecapital.com/essential-cheat-sheets-for-machine-learning-and-deep-learning-researchers-efb6a8ebd2e5) is a similar reference for machine learning (ML) and deep learning.

##  Programming
* Start using github. It is excellent for version control and for sharing. Consider how many times you have written a script called analysis_v5_final_reallyfinal_thistime_final.py. With github you will just have analysis.py. With github, other researchers can replicate exactly what you did. This will ultimately save you time, if someone emails you for example.

* A lot of open software that is developed for neuroscience runs on either Linux or OSX but not Windows. So consider installing Linux. [Ubuntu](https://help.ubuntu.com/lts/installation-guide/) is a popular distribution that has extensive support if you get stuck.

* After installing Linux, learn the [art of the command line](https://github.com/jlevy/the-art-of-command-line)

* Do you use Matlab? It is worth considering a switch to [Python](https://www.python.org/). Python offers simpler syntax, enables system wide interfacing, is open source, free and for these reasons is being used by more and more scientists. Replication is far easier with Python than Matlab.

* Want to learn Python?
  * Start with [Learn Python the Hard Way](https://learnpythonthehardway.org/book/). 52 exercises spanning installing Python to building a web app. Everyone in our lab who learned python used this tutorial.
  * Install [Anaconda](https://www.continuum.io/downloads) which is a scientific distribution of python that enables high performance computing and analysis.
  * Learn numpy with [these 100 exercises](https://github.com/rougier/numpy-100/blob/master/100%20Numpy%20exercises%20no%20solution.ipynb) written by Nicolas Rougier.
  * Become a python data ninja. Thomas Wiecki provides a [great introduction](http://nbviewer.jupyter.org/format/slides/github/twiecki/pydata_ninja/blob/master/PyData%20Ninja.ipynb#/) to data science in python.

* Need to sync files across your various lab computers/clusters and laptop you use at home and don't want to use Dropbox? Use [rsync](https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-on-a-vps) instead. e.g:
```bash
rsync -zavr -e ssh --delete --include '*/' --include='*include_these_files.[ext]' --exclude='*' [local_dir] [remote_server]:[remote_dir]
```

* Use hotkeys for [google](https://support.google.com/chrome/answer/157179?hl=en), [gmail](https://support.google.com/mail/answer/6594?co=GENIE.Platform%3DDesktop&hl=en), [atom](https://github.com/nwinkler/atom-keyboard-shortcuts), [jupyter notebooks](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/) & and  [bash](https://ss64.com/bash/syntax-keyboard.html). Consider a mechanical keyboard so your labmates love you, then hotkey some more.

* Not sure how to code something? It may have an answer on [stack overflow](https://stackoverflow.com/). Even professional programmers use stack overflow.

* Access anything or anywhere on your computer with minimal effort using Keyboard launchers like [Albert](https://github.com/albertlauncher/albert) for linux and [Alfred](https://www.alfredapp.com/) for mac.

* Learn how to properly simulate data and make sure that your analysis works the way you think that it is working.

* A basic understanding of [data structures](https://medium.freecodecamp.org/10-common-data-structures-explained-with-videos-exercises-aaff6c06fb2b) is useful for optimizing larger scale projects.

##  Generating Publication Quality Figures
* If you followed the programming advice above, you are now convinced that Python is your favorite language. Python has excellent data visualization built off [matplotlib](http://pbpython.com/effective-matplotlib.html) and a library called [seaborn](http://seaborn.pydata.org/index.html).

* Use whatever software you are using to get the figure as close to final as possible. Sometimes it is necessary to do some post edits in illustrator/inkscape but with diligent coding, you can usually avoid this, which will ultimately save you time.

* Carefully consider the colors and colormaps of your figures. How would color blind readers interpret your figures?

* Understand why people hate the [jetmap colormap](https://jakevdp.github.io/blog/2014/10/16/how-bad-is-your-colormap/). Read about different colormaps [here](https://matplotlib.org/users/colormaps.html).

* If you use Maltab, try out the [gramm toolbox](https://github.com/piermorel/gramm), inspired by R's ggplot2. 

* Save your figures in svg, or eps. pngs do not scale well.

##  Statistical Analysis
* If you are new to statistics, start [here](http://students.brown.edu/seeing-theory/) to grok the fundamentals.

* Learn to love Bayesian statistics, if you don't already.
[This](http://jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/) is an introduction on bayesian vs. frequentist statistics written by [Jake Vanderplas](https://staff.washington.edu/jakevdp/), an astrophysicist and python developer.

* Beware of p-values and null hypothesis significance testing (NHST) the de facto standard in neurobio research and cognitive neuroscience. Read [this](http://ejwagenmakers.com/2007/pValueProblems.pdf) paper for some of the problems with p-values if you are not familiar with the controversy. See [here](http://www.stat.columbia.edu/~gelman/research/published/pvalues3.pdf) and [here](http://www.stat.columbia.edu/~gelman/research/published/retropower20.pdf) for more detail. Confused about what to do now? Andrew Gelman sheds some light [here](http://www.stat.columbia.edu/~gelman/research/published/incrementalism_3.pdf) and also [here](http://www.stat.columbia.edu/~gelman/research/published/retropower20.pdf) on ways to proceed.

* As soon as possible, understand
  * [bootstraping](https://en.wikipedia.org/wiki/Bootstrapping_(statistics)),
  * [cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) and
  * [permutation tests](https://en.wikipedia.org/wiki/Resampling_(statistics)).
  * [Here](https://docs.google.com/presentation/d/11TozBxAaON1eFXeL6aK1USLtJyAbUaHhskcPkI0FLbc/edit#slide=id.g138cbbed1a_0_0 ) are some lecture notes that look at these topics in the context of multivariate pattern analysis in fMRI.

* [Rob Kass](http://www.stat.cmu.edu/~kass/), @CMU statistics, has written the extremely useful [Ten Simple Rules for Effective Statistical Practice](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004961).

* There are many texts on data analysis, but Cosma Shalizi offers a unique perspective in this [textbook](http://www.stat.cmu.edu/~cshalizi/ADAfaEPoV/ADAfaEPoV.pdf)

* Understand the bias/variance [trade off](https://ml.berkeley.edu/blog/2017/07/13/tutorial-4/)

* Do you know what the chris rock effect is in statistics? Expand your statistical lexicon [here](http://andrewgelman.com/2009/05/24/handy_statistic/).

* Are you still not using hierarchical Bayes? Everything is a trivial case of hierarchical Bayesian inference. Thomas Wiecki will show you the [way](http://twiecki.github.io/blog/2017/02/08/bayesian-hierchical-non-centered/).

* Frequent [datatau](http://www.datatau.com/) for interesting news on data analysis.

* Your stats question may have an answer over [here](https://stats.stackexchange.com/) on cross-validated.

  ###  Statistics blogs
  * [While my MCMC gently samples](http://twiecki.github.io/)

  * [Pythonic perambulations](http://jakevdp.github.io/)

  * [Statistical Modeling, Causal Inference, and Social Science](http://andrewgelman.com/)

  * Wagenmakers new blog: [Bayesian Spectacles](https://www.bayesianspectacles.org)

##  Writing Papers
* See these [Ten simple rules for structuring papers](http://biorxiv.org/content/biorxiv/early/2016/11/28/088278.full.pdf
), written by [Konrad Kording](http://koerding.com/) and Brett Mensh.

* Publish your paper to one of the [arXivs](http://www.biorxiv.org/submit-a-manuscript). If your PI doesn't support that, convince them.

* Share your work with your friends as well as your enemies, the latter might give you even better criticism.

* Steven Pinker has some interesting thoughts on how to make academic writing [better](http://stevenpinker.com/files/pinker/files/why_academics_stink_at_writing.pdf)

* If you are struggling to write scientific papers in word, e.g. embedding equations, consider using [Latex](https://www.latex-project.org) (pronounced "Lay-Tech"). Latex allows you to focus on writing rather than formatting.

##  Doing fMRI
* Know your neuroanatomy. Julian Caspers, a neuroradiologist, provided a great set of [guidelines](https://www.humanbrainmapping.org/files/2017/ED%20Courses/Course%20Materials/Anatomy_Caspers_Julian.pdf) at the 2017 Organization for Human Brain Mapping conference.

* Standardize your imaging data set using the [BIDS format](http://bids.neuroimaging.io/) - this will make your data more accessible to both your collaborators and the field at large.

* As a benchmark, you should be able to write down the [general linear model](http://www.brainvoyager.com/bvqx/doc/UsersGuide/StatisticalAnalysis/TheGeneralLinearModel.html) you are using from scratch and solve it in closed form.

* Understand the difference between [univariate and multivariate approaches](https://arxiv.org/pdf/1603.01857.pdf) to fMRI

* Next learn [representational similarity analysis](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005508) & the related [crossnobis](https://arxiv.org/ftp/arxiv/papers/1608/1608.02027.pdf) distance measure, a powerful framework that can bridge behavior, imaging, and computational models.  


* [PyCortex](https://github.com/gallantlab/pycortex) provides excellent visualization of your statistical maps projected on the surface and dynamically generated in your browser.

* Improve your understanding of anatomy with the web based user interface for exploring the human brain called [Cortical Explorer](http://corticalexplorer.com).

##  Analyzing Ephys data
* Most ephys lab use in house analysis routines in (sometimes) relatively closed source and (oftentimes) expensive applications. Pavan Ramkumar @KordingLab has written an excellent open source [package](https://github.com/KordingLab/spykes) for spike data analysis and visualization in Python.

##  Biophysical and molecular modeling
* Start [here](http://mmbios.org/index.php/software#anm) for a variety of software resources on realistic cellular, especially [MCell](http://www.mcell.org/index.html) and [NEURON](https://www.neuron.yale.edu/neuron/courses).

* Check out [CellBlender](https://github.com/mcellteam/cellblender) for visualization and simulation of realistic 3D cellular models.

* Keep a digital lab notebook with [Benchling](https://benchling.com/academic), free for academics.

* Try [ApE](http://biologylabs.utah.edu/jorgensen/wayned/ape/) for creating plasmid maps/visualization of restriction sites and planning experiments.

* Recreate expensive hardware on the cheap with [labrigger](http://labrigger.com/blog/)

* [Fiji](https://fiji.sc/) is a free and easy to use image processsor.

##  Literature Search
* You will need a citation manager early on, [PaperPile](https://paperpile.com) is a good one that is well integrated with Pubmed

* Find articles before they are officially published on [arxiv](http://biorxiv.org/)

* You can search the literature with [Pubmed](https://www.ncbi.nlm.nih.gov/pubmed/) & [Google-scholar](https://scholar.google.com). Now is a good time to make your own google scholar account if you don't have one. Also, stay on top of your favorite authors' publications with [Google-scholar's alerts](https://scholar.google.com/scholar_alerts?view_op=list_alerts&hl=en).

* Before you start down some major project that you will be committed to for years, understand the current literature in your topic. Understand very clearly why you are going to do what you are going to do.

* Be skeptical of author's use of the word prediction, often what they really mean is in-sample linear correlation, and not what prediction actually means, out-of-sample generalization of a model. [Here](http://pilab.psy.utexas.edu/publications/Yarkoni_Westfall_PPS_in_press.pdf) Tal Yarkoni provides some insights.


## Grant writing
* Be aware of what grants have been funded in your field, by searching [nih reporter](https://projectreporter.nih.gov/reporter.cfm). This will tell you what was funded, the program officer, the PI, etc.

## Twitter is a great resource for identifying new papers, events, tips etc.
* [@tdverstynen](https://twitter.com/tdverstynen)  cognitive neuroscience, theoretical neuroscience, imaging (DSI/fMRI)
* [@KordingLab](https://twitter.com/kordinglab)  neural data science, computational modeling
* [@StatModeling](https://twitter.com/StatModeling)  statistics, hierarchical bayesian modeling, R
* [@NKriegeskorte](https://twitter.com/NKriegeskorte)  fMRI, RSA, deep learning
* [@jakevdp](https://twitter.com/jakevdp)  python, data analysis, astrophysics
* [@fonnesbeck](https://twitter.com/fonnesbeck) statistical analysis in python
* [@bioRxiv Neuroscience](https://twitter.com/biorxiv_neursci) the Rxiv for neuro
* [@Neuro_Skeptic](https://twitter.com/Neuro_Skeptic)  neuroscience in general
* [@BLAMlab](https://twitter.com/blamlab?lang=en) stroke recovery, motor control
* [@diedrichsenlab](https://twitter.com/diedrichsenlab) computational neuroimaging   

## Papers
* [Neuroscience Needs Behavior](http://www.cell.com/neuron/pdf/S0896-6273(16)31040-6.pdf)
* [Could a Neuroscientist Understand a Microprocessor](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005268)

##  Meetings
* Never show up empty handed to meetings with your PI.
* Have a clear objective to all meetings that everyone else knows as well.
* Be able to show some evidence of your productivity.

* You will have some days or weeks where nothing worked. I found that in those cases it is productive to have a "rainy day" folder containing interesting analyses/figures you have not yet shown.

## Guides
* Learn how to learn with [this](https://www.coursera.org/learn/learning-how-to-learn) coursera course
* Have a long look at this [Survival Guide](http://karpathy.github.io/2016/09/07/phd/) for PH.d students, by Andrej Karpathy, CS Ph.D, and the current director of AI at Tesla.
* Ronald Azuma's [retrospective](http://www.cs.unc.edu/~azuma/hitch4.html) on graduate school
* Randy Pausch on [time management](https://www.youtube.com/watch?v=oTugjssqOT0)

## Acknowledgments
Thanks to contributions from Ran Liu, Annie Homan, Rory Flemming, and Daniel Borek for making this page more useful.
