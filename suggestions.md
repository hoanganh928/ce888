# Assignment Suggestions

Below you will find a list of potential projects suitable for CE888. Each project has a number of core references and a data source that you should
read and evaluate. Your goal should be to identify a project that should both align nicely with your personal interests and qualifies as "data science-y" 
enough to be considered appropriate for the module. The write-up of your project would need to follow the template of a relevant conference or journal paper and the focus 
should be on quality rather than quantity. A minimum of amount of novelty is expected at each project and toy problems are not acceptable - if you help deciding on which project to work, please talk to the module supervisor. 


### Role Playing Games: systems and statistics.
A massive number of gaming systems has been proposed that range from the heavy dice pools of Shadowrun and World of Darkness to the percentile system of Eclipse Phase and Call of Cthulhu. The goal of the project is to analyse the statistical qualities of these games systems (means, medians, standard errors, variances, roll distributions etc. ) and identify possible "black spots" in game design (e.g. do we get games with heavy tailed distributions? Do the mechanics of most games fail to correctly simulate certain events?)

**References:**

1. [Isaksen, Aaron, et al. "Characterising Score Distributions in Dice Games." Game and Puzzle Design Journal, 2016 ](http://julian.togelius.com/Isaksen2016Characterising.pdf)
2. [A Treatise on Different Dice-rolling Mechanics in RPGs](http://rpg-design.wikidot.com/evaluation)


**Target Journal/Conference:** gapdjournal.com

**Example Data:** You would need to have an interest and understanding of Role Playing Games so as to be able to at least appreciate major game systems. 

* * *
### Intransitivities

It is often the case that we would like to organise tournaments where players of the same or similar skill are matched to one another. A phenomenon that has been observed in artificial systems is the intransitivity of skill between players. For example, let us assume that player A beats player B and that player B beats player C - one would normally conclude that A beats C. However this might not be the case, as certain qualities of player C might make it extremely advantageous against player A. The aim of this project is to identify how often intransitivities occur in real computer (or otherwise) games between players and if persistent intransitivities tell us anything about the structure of a game and the players that play it. 

**References:**

1. [Samothrakis, Spyridon, et al. "Coevolving game-playing agents: Measuring performance and intransitivities." IEEE Transactions on Evolutionary Computation 17.2 (2013): 213-226.](http://ieeexplore.ieee.org/document/6242396/)
2. [Glickman, Mark E. "A comprehensive guide to chess ratings." American Chess Journal 3 (1995): 59-102.](http://www.glicko.net/research/acjpaper.pdf)
3. [Herbrich, Ralf, Tom Minka, and Thore Graepel. "Trueskill™: A Bayesian skill rating system." Advances in neural information processing systems. 2006.](http://machinelearning.wustl.edu/mlpapers/paper_files/NIPS2006_688.pdf)

**Target Journal/Conference:** IEEE CIG

**Example Data:** [Dota 2 Matches](https://www.kaggle.com/devinanzelmo/dota-2-matches). 

* * *


### RL and Interpretability

Modern Reinforcement Learning helps agents learn how to act using complex patterns of text, sound and video and it's slowly moving away from research and making inroads to traditional industries (e.g., creating game NPC characters). The high dimensionality of the input space makes it however very hard to interpret why an agent preferred one action over another. In this project we will try to transfer some novel methods from supervised learning to Reinforcement Learning  in order to interpret why agents make certain decisions. We will use already existing Atari game playing agents and try to interpret their actions profile in real time, effectively "seeing" through the agent's eyes.

**References:**

1. [Ribeiro, Marco Tulio, Sameer Singh, and Carlos Guestrin. "" Why Should I Trust You?": Explaining the Predictions of Any Classifier." KDD (2016).](https://arxiv.org/pdf/1602.04938v3)
2. [Lipton, Zachary C., et al. "The Mythos of Model Interpretability." IEEE Spectrum (2016)](http://zacklipton.com/media/papers/mythos_model_interpretability_lipton2016.pdf)

**Target Journal/Conference:** IEEE CIG/TCAIG/Neural Networks

**Example Data:** 

1. [Example Open AI gym Atari Controllers](https://github.com/ppwwyyxx/tensorpack/tree/master/examples/OpenAIGym)
2. [Lime](https://github.com/marcotcr/lime)
3. [Example Open AI agent playing breakout](https://gym.openai.com/evaluations/eval_L55gczPrQJamMGihq9tzA)

* * *

### Head bootstrap vs Dropout

Dropout is a well understood method for regularising neural networks. Outside neural networks, a framework commonly used for achieving similar (but not quite the same) results is "bagging". Unfortunately, one has to train multiple neural networks in order to gain the advantages of bagging, a process that is very slow. Recently, in the context of Reinforcement Learning, an algorithm has been proposed where multiple output layers of a neural network are trained in parallel using bootstrapping, while the core network remains the same. This project will evaluate this configuration in supervised learning problems.

**References:**

1. [Osband, Ian, et al. "Deep Exploration via Bootstrapped DQN." arXiv preprint arXiv:1602.04621 (2016).](http://arxiv.org/pdf/1602.04621)
2. [Single estimator versus bagging: bias-variance decomposition](http://scikit-learn.org/stable/auto_examples/ensemble/plot_bias_variance.html#sphx-glr-auto-examples-ensemble-plot-bias-variance-py)
3. [The Bagging Classifier](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.BaggingClassifier.html#sklearn.ensemble.BaggingClassifier)

**Target Journal/Conference:** IEEE Transactions on Neural Networks and Learning Systems

**Example Data:** 

1. [Example MNIST MLP for Keras](https://github.com/fchollet/keras/blob/master/examples/mnist_mlp.py)
2. [Example CIFAR-10 for Keras](https://github.com/fchollet/keras/blob/master/examples/cifar10_cnn.py)

* * *

### Cause and effect 

Understanding cause from effect in pairs of data is of paramount importance; for example one might want to understand if the raise in height is causing a drop in temperature or the other way around. This project will try to learn the causal direction of cause-effect pairs using recurrent neural networks. Data is presented as a set of collected datapoints (not a sequence, but we will treat it is us such) of various lengths and recurrent neural network should be trained to infer the causal direction of the data. 

**References:**

1. [Sequence Classification with LSTM Recurrent Neural Networks in Python with Keras](http://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/)
2. [Distinguishing cause from effect using observational data: methods and benchmarks](https://arxiv.org/pdf/1412.3773v3.pdf)

**Target Journal/Conference:** IEEE Transactions on Knowledge and Data Engineering

**Example Data:** 

1. [Cause and effect pairs](http://webdav.tuebingen.mpg.de/cause-effect/)
2. [Cause and effect pairs file to be used in experiments](http://webdav.tuebingen.mpg.de/cause-effect/pairs_1.0.zip)

* * *

### Bootstrapping for polling 

It has been hypothesised that recent (repeated) poll failures have to do with three key assumptions a) that the "undecided" crowd will invariably move towards the status quo b) that voters are not lying on purpose or out of fear c) that no section of the demographic is completely missing from the poll. This project will try to align polling results with demographic data using a biased version of bootstrapping, where one should try to re-sample (and thus present to a learning algorithm) sampling points according to how often we assume they occur in the general population. 

**References:**

1. [Online Bagging and Boosting](http://ieeexplore.ieee.org/document/1571498/)
2. [Similarity Measures](http://www.scholarpedia.org/article/Similarity_measures)

**Target Journal/Conference:** IEEE Transactions on Knowledge and Data Engineering

**Example Data:** Identify an event of interest to you (e.g. elections) and find polling data from it, preferably ones that have the demographic characteristics of the people polled. 

* * *


### Artificial Intelligence and society 

There is an active debate on what the impact of the raise of artificial intelligence will be on labour and labour time. One could possibly use data from previous industrial revolutions
and try to make a coherent argument on whether labour hours will go up or down as a result of improved machinery (i.e. intelligent machines). This is a "small data" project and methods tailored to smaller datasets should be used - examples in the references below.

**References:**

1. [Joy, Bill. "Why the future doesn’t need us." Nanoethics. The Ethical and Social Implications of Nanotechnology (2000): 17-30.](http://xa.yimg.com/kq/groups/20503014/322130564/name/ch3.pdf)
2. [Pre-industrial workers had a shorter workweek than today's](http://groups.csail.mit.edu/mac/users/rauch/worktime/hours_workweek.html)
3. [Example of time series analysis](http://scikit-learn.org/stable/auto_examples/gaussian_process/plot_compare_gpr_krr.html)

**Target Journal/Conference:** Journal of Artificial Intelligence Research, AI and Society track

**Example Data:** See the second reference above, but also you probably need to discover data online. 

* * *


### Question Answering using Random Forests 

Random Forests are a machine learning method that is trivially parallelisable and extremely fast to train. With the advent of word2vec, one has a mechanism that can extract the semantic meaning of words directly, by having them converted into vector representations. For this project we will use random forests directly on word2vec sequences on the bABi tasks, a set of question answering tasks for Artificial Intelligence. You will not need to actually use any word2vec method for this project, just to convert tasks sentences to fixed length representations of vectors and feed them to a Random Forest. 

**References:**

1. [Weston, Jason, et al. "Towards ai-complete question answering: A set of prerequisite toy tasks." arXiv preprint arXiv:1502.05698 (2015).](https://arxiv.org/pdf/1502.05698v10)
2. [Mikolov, Tomas, et al. "Distributed representations of words and phrases and their compositionality." Advances in neural information processing systems. 2013.](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)

**Target Journal/Conference:** IEEE Transactions on Knowledge and Data Engineering 

**Example Data:** 

1. [bAbi Tasks](http://www.thespermwhale.com/jaseweston/babi/tasks_1-20_v1-2.tar.gz)
2. [Glove Vectors](http://nlp.stanford.edu/projects/glove/)


* * *

* * *

