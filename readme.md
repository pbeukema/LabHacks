## Table of Contents
* [Open science](#open-science-opsci-essentials)
* [Data Analysis](#data-analysis)   
* [Programming](#programming)   
* [Making figures nice](#generating-publication-quality-figures)    
* [Statistics](#statistical-analysis)      
* [fMRI](#fmri)  
* [Ephys](#analyzing-ephys-data)  
* [Biophysical modeling](#biophysical-and-molecular-modeling)
* [Lit search](#literature-search)  
* [Writing papers](#writing-papers)   
* [Giving talks](#giving-talks)   
* [Grant Writing](#grant-writing)  
* [Meetings](#meetings-with-your-pi)     
* [Meta Neuro Papers](#papers)  
* [Survival Guides](#survival-guides)
* [Science Blogs](#science-blogs)
## Open science (opsci) essentials
* For better or worse, you probably want a website at this stage of human evolution, where you can link to free pdfs of your manuscripts, reference code, publish datasets, point people to X project, etc. The fastest (<1 hr), simplest (4 steps), and most elegant way I have come across is through [github pages](https://pages.github.com) using [jekyll themes](http://jekyllthemes.org). The following steps walk you through hosting your new website on your github account, which you will create in step 1 if you don't already have one. N.B. You do not need to install anything locally on your machine (and it is likely preferable not to) regardless if you are using Linux, OSX or Windows. The following steps are sufficient.  
    1. Sign up for [github](https://github.com) if you do not have an account.  
    2. [Fork](https://help.github.com/articles/fork-a-repo/) a jekyll repository to get an academic template on your account (e.g. fork this [repo](https://github.com/alshedivat/al-folio) and your site will look like [this](https://pbeukema.github.io)). 
    3. Rename the repository you just forked to [username].github.io. [username] is your username from step 1.  
    4. Edit the data in the pages directory and config.yml files to suit your needs. 
    * Go to your website (which will live at https://[username].github.io). 
    
* [Standardize](https://github.com/drivendata/cookiecutter-data-science) your project structure. Share with your colleagues. Be transparent. Following two lines will get you set up. 
```quick version
pip install cookiecutter 
cookiecutter https://github.com/drivendata/cookiecutter-data-science
```
    
* Need to get a paper but behind a paywall? Try sci-hub. If [this](https://sci-hub.la) link is broken look on the right side of the [wikipedia page](https://en.wikipedia.org/wiki/Sci-Hub) for up-to-date links.  


## Data analysis 
* Download [Atom](https://atom.io/). It is a very powerful and free! editor that integrates nicely with github.
Use it for writing text, markup, code, scripts, etc.

* Use [jupyter notebooks](http://jupyter.readthedocs.io/en/latest/index.html) for development and for analysis pipelines. Install [Kyle Dunovan's](https://github.com/dunovank) [jupyter themes](https://github.com/dunovank/jupyter-themes) to make your notebooks pretty and work faster.

* Consider [version-controlling your data](https://dataversioncontrol.com/) along with your [code](https://github.com). 

* Make an "autopilot" script for your analyses, so that figures can be updated in real time. Then write a [cron job](https://healthchecks.io/docs/cron/) to execute the analysis script so that newly collected data is automatically integrated perhaps with an email summarizing the results sent to you or your advisor. Example [here](https://github.com/pbeukema/rsaRemap/blob/master/modmap_autopilot.py).

* Make a startup file for your jupyter notebooks that preloads modules like numpy and scipy and figure specifications so they are consistent and pub ready. The config file can specify font sizes, legends, color themes etc.

* Learning data science? [Here](https://unsupervisedmethods.com/cheat-sheet-of-machine-learning-and-python-and-math-cheat-sheets-a4afe4e791b6) is an extremely well curated series of quick references for data science in python (numpy, scipy, pandas), ML algorithms, probability and more

* Diving into deep learning? [Here](https://startupsventurecapital.com/essential-cheat-sheets-for-machine-learning-and-deep-learning-researchers-efb6a8ebd2e5) is a similar reference for machine learning (ML) and deep learning.

##  Programming
* Start using github. It is excellent for version control and for sharing. Consider how many times you have written a script called analysis_v5_final_reallyfinal_thistime_final.py. With github you will just have analysis.py. With github, other researchers can replicate exactly what you did. This will ultimately save you time, if someone emails you for example.
* If you write software for the use of the greater scientific community, it will be a lot easier for others to port your code and collaborate if you follow a standard set of guidelines when packaging your project for release (e.g. on github). Here is a [template](https://github.com/uwescience/shablona) to follow written by Ariel Rokem. 

* A lot of open software that is developed for neuroscience runs on either Linux or OSX but not Windows. So consider installing Linux. [Ubuntu](https://help.ubuntu.com/lts/installation-guide/) is a popular distribution that has extensive support if you get stuck.

* After installing Linux, learn the [art of the command line](https://github.com/jlevy/the-art-of-command-line)

* Do you use Matlab? It is worth considering a switch to [Python](https://www.python.org/). Python offers simpler syntax, enables system wide interfacing, is open source, free and for these reasons is being used by more and more scientists. Replication is far easier with Python than Matlab.

* Now want to learn Python?
  * Everyone in our lab learned the basic syntax with [Learn Python the Hard Way](https://learnpythonthehardway.org/book/). 52 exercises spanning installing Python to building a web app. 
  * Here is a [Python Bootcamp notebook](https://github.com/TomDonoghue/PythonBootcamp/blob/master/ProgrammingWithPython.ipynb) that provides excellent advice on learning Python, written by Tom Donoghue. 
  * Read the [style guide](https://www.python.org/dev/peps/pep-0008/) to write "pythonic" code. 
  * Install [Anaconda](https://www.continuum.io/downloads) which is a scientific distribution of python that enables high performance computing and analysis.
  * Package your python project with this amazing [guide](http://veekaybee.github.io/2017/09/26/python-packaging/) by Vicki Boykis
  * Learn numpy (a package for scientific computing) with [these 100 exercises](https://github.com/rougier/numpy-100/blob/master/100%20Numpy%20exercises%20no%20solution.ipynb) written by Nicolas Rougier.
  * Become a python data ninja. Thomas Wiecki provides a [great introduction](http://nbviewer.jupyter.org/format/slides/github/twiecki/pydata_ninja/blob/master/PyData%20Ninja.ipynb#/) to data science in python.
  

* Use hotkeys for [google](https://support.google.com/chrome/answer/157179?hl=en), [gmail](https://support.google.com/mail/answer/6594?co=GENIE.Platform%3DDesktop&hl=en), [atom](https://github.com/nwinkler/atom-keyboard-shortcuts), [jupyter notebooks](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/) & and  [bash](https://ss64.com/bash/syntax-keyboard.html). Consider a mechanical keyboard so your labmates love you, then hotkey your keyboard to eliminate typing entirely.

* Not sure how to code something? It may have an answer on [stack overflow](https://stackoverflow.com/). Even professional programmers use stack overflow.

* Access anything or anywhere on your computer with minimal effort using Keyboard launchers like [Albert](https://github.com/albertlauncher/albert) for linux and [Alfred](https://www.alfredapp.com/) for mac.

* Learn how to simulate data to ensure that your analysis works the way you think it does.

* A basic understanding of [data structures](https://medium.freecodecamp.org/10-common-data-structures-explained-with-videos-exercises-aaff6c06fb2b) is useful for optimizing larger scale projects.

* Need to sync files across your various lab computers/clusters and laptop you use at home and don't want to use Dropbox? Use [rsync](https://www.digitalocean.com/community/tutorials/how-to-use-rsync-to-sync-local-and-remote-directories-on-a-vps) instead. e.g:
```bash
rsync -zavr -e ssh --delete --include '*/' --include='*include_these_files.[ext]' --exclude='*' [local_dir] [remote_server]:[remote_dir]
```

##  Generating publication quality figures
* First read these [ten rules for better figures](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003833) (and accompanying [source code](https://github.com/rougier/ten-rules))
* If you followed the programming advice above, you are now convinced that Python is your favorite language. Python has excellent data visualization built off [matplotlib](http://pbpython.com/effective-matplotlib.html) and a library called [seaborn](http://seaborn.pydata.org/index.html).

* Use your plotting software of choice (e.g. seaborn) to get your figure as close to final as possible. Avoid having to make post-edits in illustrator/inkscape which can be a huge time sink as a graduate student.

* Carefully consider the colors and colormaps of your figures. How would color blind readers interpret your figures?

* Understand why people hate the [jetmap colormap](https://jakevdp.github.io/blog/2014/10/16/how-bad-is-your-colormap/). Read about different colormaps [here](https://matplotlib.org/users/colormaps.html).

* If you use Matlab, try out the [gramm toolbox](https://github.com/piermorel/gramm), inspired by R's ggplot2. 

* Have a look at the tutorials on [flowingdata](http://flowingdata.com/) for excellent data visualization.

* Save your figures in svg, or eps, not png. 

##  Statistical analysis
* Learning statistics or want to brush up? Here are three textbooks (available online) that you can choose from depending on the depth you want to explore and mathematical background you have. 
  * [Stats without Tears](https://www.ic.unicamp.br/~wainer/cursos/1s2013/ml/livro.pdf) -- cover the fundamentals, requires little mathematical background 
  * [All of Statistics](https://www.ic.unicamp.br/~wainer/cursos/1s2013/ml/livro.pdf) -- more detailed than above, requires calculus and linear algebra
  * [Advanced data analysis](http://www.stat.cmu.edu/~cshalizi/ADAfaEPoV/ADAfaEPoV.pdf) -- if you dream about distributions, requires substantial statistical background 
* If you are teaching statistics, [here](http://students.brown.edu/seeing-theory/) are excellent visualizations of core concepts.

* See this [tutorial](http://m-clark.github.io/documents/) on machine learning concepts.  

* Learn to love Bayesian statistics, if you don't already. Read [this](http://jakevdp.github.io/blog/2014/03/11/frequentism-and-bayesianism-a-practical-intro/) introduction on bayesian vs. frequentist statistics written by [Jake Vanderplas](https://staff.washington.edu/jakevdp/), an astrophysicist and python developer. 

* Looking for a Bayesian analysis package? Try [JASP](https://jasp-stats.org/).

* Beware of p-values and null hypothesis significance testing (NHST) the de facto standard in neurobiology, cognitive neuroscience and much of biomedical research:
  * [Beyond the dead salmon](https://slides.com/neuro_logical/pvps): talk on p-values and how it relates to the current reproducibility crisis and pragmatic approaches to the problem. 
  * Regina Nuzzo on how not to get fooled by p-values: [video](https://videocast.nih.gov/summary.asp?Live=26200&bhcp=1Read)
  * Problems with p-values: [1](http://ejwagenmakers.com/2007/pValueProblems.pdf) [2](https://peerj.com/articles/3544.pdf)
  * How to proceed: [Abandon statistical thresholds](http://www.stat.columbia.edu/~gelman/research/unpublished/abandon.pdf)
* Do you have multi-level data? E.g. do you have some cells from one animal and some other cells from a different animal? Are you pooling the data because they have similar distributions/variance? Instead you might want to consider [hierarchical](https://en.wikipedia.org/wiki/Multilevel_model) aka mixed effect models. [Here](http://mfviz.com/hierarchical-models/) is a really beautiful demonstration of this concept.   
* As soon as possible, understand:
  * [bootstrapping](https://en.wikipedia.org/wiki/Bootstrapping_(statistics)) -- insanely powerful. 
  * [cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) -- enables generalization
  * [permutation tests](https://en.wikipedia.org/wiki/Resampling_(statistics)) -- gets you a null distribution, sometimes hard to analytically derive in closed form
  * [Here](https://docs.google.com/presentation/d/11TozBxAaON1eFXeL6aK1USLtJyAbUaHhskcPkI0FLbc/edit#slide=id.g138cbbed1a_0_0 ) are some lecture notes that look at these topics in the context of multivariate pattern analysis in fMRI.
   
*	Do not let your test data into your training data (i.e. double dipping)

* [Rob Kass](http://www.stat.cmu.edu/~kass/), @CMU statistics, has written the extremely useful [Ten Simple Rules for Effective Statistical Practice](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004961).


* Understand the bias/variance [trade off](https://ml.berkeley.edu/blog/2017/07/13/tutorial-4/)

* Do you know what the chris rock effect is in statistics? Expand your statistical lexicon [here](http://andrewgelman.com/2009/05/24/handy_statistic/).

* Are you still not using hierarchical Bayes? Thomas Wiecki will show you the [way](http://twiecki.github.io/blog/2017/02/08/bayesian-hierchical-non-centered/). [Everything is a trivial case of hierarchical Bayesian inference](https://twitter.com/farlkriston/status/699515098050723840). 

* Frequent [datatau](http://www.datatau.com/) for interesting news on data analysis.

* Your stats question may have an answer over [here](https://stats.stackexchange.com/) on cross-validated.

  ###  Statistics blogs
  * [While my MCMC gently samples](http://twiecki.github.io/)

  * [Pythonic perambulations](http://jakevdp.github.io/)

  * [Statistical Modeling, Causal Inference, and Social Science](http://andrewgelman.com/)

  * Wagenmakers new blog! [Bayesian Spectacles](https://www.bayesianspectacles.org)

##  Writing papers
* See these [Ten simple rules for structuring papers](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005619
), written by [Konrad Kording](http://koerding.com/) and Brett Mensh.
* Omit needless words, suppress the encyclopedic impulse, don't try to sound smart, and other sound [advice](https://golem.ph.utexas.edu/category/2017/12/on_writing_short_papers.html) from a mathematician.

* Andrew Gelman provides some more general advice for academic writing [here](http://andrewgelman.com/2009/07/30/advice_on_writi/). 

* Publish your paper to one of the [arXivs](http://www.biorxiv.org/submit-a-manuscript). If your PI doesn't support that, convince them.

* If you are frustrated with writing, read [this](http://lithub.com/how-academics-survive-the-writing-grind-some-anecdotal-advice/)
* Share your work with your friends as well as your enemies, the latter might give you even better criticism.

* Steven Pinker has some interesting thoughts on how to make academic writing [better](http://stevenpinker.com/files/pinker/files/why_academics_stink_at_writing.pdf)

* If you are struggling to write scientific papers in word, e.g. embedding equations, consider using [Latex](https://www.latex-project.org) (pronounced "Lay-Tech"). Latex allows you to focus on writing rather than formatting.

## Giving talks
* You need to choose some medium of presenting your slides. It would be nice to always have access to them, to be able to share them with others who might not have your software (e.g. powerpoint) and to be easily viewable on mobile. [Here](http://slides.com) is a cross-platform tool that meets those needs.  

* It is very challenging to give high-quality talks and everyone struggles with it. A lot of academics do not receive training on how to give talks and do not know the most effective ways of presenting information - but this has been looked at. [Here](http://static.duarte.com/Slideology_Sample30.pdf) are some incredibly useful notes how to prepare the actual content of the slides, and  [here](https://www.youtube.com/watch?v=Hp7Id3Yb9XQ) are some notes on the speaking portion. 

##  fMRI

* Know your neuroanatomy. Julian Caspers, a neuroradiologist, provided a great set of [guidelines](https://www.humanbrainmapping.org/files/2017/ED%20Courses/Course%20Materials/Anatomy_Caspers_Julian.pdf) at the 2017 Organization for Human Brain Mapping conference. You also may find this interactive [brain explorer](http://www.brainfacts.org/3D-Brain#intro=false&focus=Brain-cerebral_hemisphere-right) useful.

* [Best practices](https://www.biorxiv.org/content/biorxiv/early/2016/07/10/054262.full.pdf) for reporting fMRI studies. 

* Neuroimaging is easy to do wrong and still get a result. [Here](https://arxiv.org/pdf/1703.06670.pdf) are common pitfalls to avoid when running your analysis.  

* It is absolutely critical to know what kind of power you have and what you can conclude from the kind of analysis that you are doing. Here is a useful [guide](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0184923). 

* Standardize your imaging data set using the [BIDS format](http://bids.neuroimaging.io/) - this will make your data more accessible to both your collaborators and the field at large.

* As a benchmark, you should be able to write down the [general linear model](http://www.brainvoyager.com/bvqx/doc/UsersGuide/StatisticalAnalysis/TheGeneralLinearModel.html) you are using from scratch and solve it in closed form.

* Understand the difference between [univariate and multivariate approaches](https://arxiv.org/pdf/1603.01857.pdf) to fMRI

* Next learn [representational similarity analysis](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005508) & the related [crossnobis](https://arxiv.org/ftp/arxiv/papers/1608/1608.02027.pdf) distance measure, a powerful framework that can bridge behavior, imaging, and computational models.  

* You will need a visualization tool. A lot of labs have success with [MRIcroGL](http://www.mccauslandcenter.sc.edu/mricrogl/home) or [the connectome workbench](https://www.humanconnectome.org/software/connectome-workbench). Recently [James Gao](http://journal.frontiersin.org/article/10.3389/fninf.2015.00023/full) written an indredibly powerful new tool called [PyCortex](https://github.com/gallantlab/pycortex) which uses WebGL to render the flat maps and fiducial surfaces in your browser, you can even project movies on the surface.  

* Improve your understanding of anatomy with the web based user interface for exploring the human brain called [Cortical Explorer](http://corticalexplorer.com).

* Before you get really deep in your design, check out [NeuroSynth](http://neurosynth.org) (written by Tal Yarkoni) to run a meta analysis on your covariates of interest to see what has been done before. 

##  MEG
*	[MNE-python](https://www.martinos.org/mne/stable/index.html) is the go-to for source localization and sensor space data processing
    
## ECoG
*	For localizing surface electrodes see this [python toolbox](https://github.com/ChangLabUcsf/img_pipe) 
    
##  Analyzing ephys data
* Most ephys lab use in house analysis routines in (sometimes) relatively closed source and (oftentimes) expensive applications. Pavan Ramkumar @KordingLab has written an excellent open source [package](https://github.com/KordingLab/spykes) for spike data analysis and visualization in Python.

##  Biophysical and molecular modeling
* Start [here](http://mmbios.org/index.php/software#anm) for a variety of software resources on realistic cellular, especially [MCell](http://www.mcell.org/index.html) and [NEURON](https://www.neuron.yale.edu/neuron/courses).

* Check out [CellBlender](https://github.com/mcellteam/cellblender) for visualization and simulation of realistic 3D cellular models.

* Keep a digital lab notebook with [Benchling](https://benchling.com/academic), free for academics.

* Try [ApE](http://biologylabs.utah.edu/jorgensen/wayned/ape/) for creating plasmid maps/visualization of restriction sites and planning experiments.

* Recreate expensive hardware on the cheap with [labrigger](http://labrigger.com/blog/)

* [Fiji](https://fiji.sc/) is a free and easy to use image processsor.

##  Literature search
* You will need a citation manager early on, [PaperPile](https://paperpile.com) is a good one that is well integrated with Pubmed
    *	[Mendeley](https://www.mendeley.com/) is a free alternative
    
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
* [@talyarkoni](https://twitter.com/talyarkoni?lang=en) imaging, meta 
* [@flowingdata](https://twitter.com/flowingdata) data visualization
* [@ShuhBillSkee](https://twitter.com/ShuhBillSkee) 

## Papers
* [Neuroscience Needs Behavior](http://www.cell.com/neuron/pdf/S0896-6273(16)31040-6.pdf)
* [Could a Neuroscientist Understand a Microprocessor](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005268)

##  Meetings
* Never show up empty handed to meetings with your PI.
* Have a clear objective to all meetings that everyone else knows as well.
* Be able to show some evidence of your productivity.
* You will have some days or weeks where nothing worked. I found that in those cases it is productive to have a "rainy day" folder containing interesting analyses/figures you have not yet shown.

## Guides
* [How to pick a graduate advisor](http://www.sciencedirect.com/science/article/pii/S0896627313009070)

* Learn how to learn with [this](https://www.coursera.org/learn/learning-how-to-learn) coursera course
* Have a long look at this [Survival Guide](http://karpathy.github.io/2016/09/07/phd/) for PH.d students, by Andrej Karpathy, CS Ph.D, and the current director of AI at Tesla.
* For U.S. graduate students especially at private institutions in 2018 and beyond, its likely going to become significantly more financially difficult because your tuition waiver is about to be considered taxable income, which means your take home pay will be reduced by some percentage (5-30%). Since personal finances are rarely addressed during the onboarding process, you must educate yourself. Here is course called [personal finance for engineers](https://cs007.blog/) from Stanford.  
* Ronald Azuma's [retrospective](http://www.cs.unc.edu/~azuma/hitch4.html) on graduate school
* Randy Pausch on [time management](https://www.youtube.com/watch?v=oTugjssqOT0)
* [Know when and when not to say no](https://web.archive.org/web/20170312041524/http:/www.brianwansink.com/phd-advice/the-grad-student-who-never-said-no)
* Find (neuro)hackathons in your area and go to them. You get to meet all kinds of people and produce something at an incredibly fast rate, thanks to the symbiosis of working on a team. Can be especially refreshing if you are spending years on your projects. 
* [Slides](https://www.slideshare.net/deevybishop/faillbility-in-science-responsible-ways-to-handle-mistakes) on making mistakes and being wrong.  
* [Guide](http://www.math.cornell.edu/~hubbard/readingmath.pdf) on reading math. 

## Science blogs
* Mark Humphries will blow up your world at [the Spike](https://medium.com/the-spike)

## Facts about Brains
* [Brain Facts and Figures](https://faculty.washington.edu/chudler/facts.html?utm_content=buffer97672&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)

## Acknowledgments
Thanks to contributions from Ran Liu, Annie Homan, Rory Flemming, Daniel Borek, and Matt Boring for making this page more useful.

