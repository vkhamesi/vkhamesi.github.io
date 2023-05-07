---
title: "Introductions"
categories:
  - General
tags:
  - Introductions
  - Background
  - Machine Learning
classes: wide
toc: true
toc_label: "Contents"
toc_icon: "bookmark"
---

# My journey to statistics and machine learning

## First research projects

### Classes préparatoires aux Grandes Écoles d'Ingénieurs

As someone with strong interests in science and mathematics, I moved from Lyon to Paris when I was 18 years old to pursue French _Classes Préparatoires aux Grandes Écoles d'Ingénieurs_ at [Lycée Janson de Sailly](https://www.janson-de-sailly.fr/#home), with a strong focus in mathematics, physics and computer science. I could work on my first research project exploring chaos theory in mathematics and physics through the logistic map and the forced oscillations pendulum ([presentation](/assets/docs/TIPE_Khamesi.pdf)). 

### Science at École Centrale de Lyon

I then joined [École Centrale de Lyon](https://www.ec-lyon.fr/en) in 2019  and specialised in applied mathematics, numerical methods, statistics, probability and machine learning while in the same time I was following core modules in science such as quantum physics or chemistry and also in engineering such as electrical engineering or fluids mechanics which provided me with a comprehensive understanding of various scientific fields. 

### My very first machine learning project

During my first year at École Centrale de Lyon, I conducted my first research project which consisted in designing a machine learning approach for solving a selection and ranking problem, supervised by [Pr Christian de Peretti](https://www.ec-lyon.fr/en/contacts/christian-peretti). We reproduced state-of-the-art algorithms from scratch instead of using libraries, including principal components analysis [[1]](#references), self-organising maps [[2]](#references) (also referred as Kohonen networks) and a novel hierarchical clustering approach based on graph theory [[3]](#references). We then applied the end-to-end approach to financial data to solve the problem of building an efficient investment portfolio, in which one first needs to pick a finite number of assets from a possibly (very) large set and then rank these assets to compute their respective weights. In fact, this is a good example where usual techniques for portfolio optimisation can not be applied since estimating covariances in high dimensions is challenging, referred as _curse of dimensionality_ [[4]](#references). This research project was awarded both by [academia](https://bibli.ec-lyon.fr/actualites/2020/prix-francis-leboeuf-2020-pe-sont-ligne), with our work being published at the university library [[5]](#references) and by industry, being ranked first at a [national competition](https://www.finance-and-innovation-for-good.com/editions-precedentes) organised by Google and others. I would approach the problem in many different ways now that I have more background in the field, but I do believe it was a very good starting point!

## Studying machine learning

### Statistics and Machine Learning at École Centrale de Lyon

My introduction to machine learning was through following the Centrale Lyon Machine Learning [module](https://machine-learning-centrale.github.io/) taught by [Pr Yohann de Castro](https://ydecastro.github.io/) and shared with [École Normale Supérieure de Lyon](http://www.ens-lyon.fr/en/). The courses were given by diving deep in fundamental concepts such as linear models, regularisation, decision trees, ensemble methods, dimensionality reduction or clustering. I really liked the way the lectures were given by explaining how things work in a big picture and then exploring the mathematical details via tutorials, and I think this is what gave me passion for understanding how machine learning algorithms work and how to reproduce them. Pr de Castro was also responsible of the core module in Probability and Statistics and I will always remember about the introduction example on interarrival bus waiting time estimation! It gave me a vision of statistics as a tool to model and extract information from collected data.

### MSc in Statistics at Imperial College London

I realised that statistics was a very wide field in mathematics and I wanted to dedicate more time studying it by pursuing the MSc in Statistics at [Imperial College London](https://www.imperial.ac.uk/). I learned more about statistical inference, computational and applied statistics, machine learning and deep learning. Among my favourite modules were the _Machine Learning_ course taught by [Dr Sarah Filippi](https://www.imperial.ac.uk/people/s.filippi) and the _Deep Learning with TensorFlow_ module taught by [Dr Kevin Webster](https://www.imperial.ac.uk/people/kevin.webster). This last course really showed me how flexible and complex deep learning architectures can be but in the same time explaining details of basic tools like automated gradients computation or backpropagation. This course covered deep learning fundamentals, but also recent advanced concepts such as computer vision, sequential modelling like natural language processing and generative approaches with their mathematical background and coding implementation.

### Learning new concepts every day

I am fueled by learning new things every day, so even after completing the MSc, I keep updating my knowledge in machine learning and deep learning by reading and reproducing scientific papers. I am interested in models explainability and the idea of building unified frameworks for explaining the output of machine learning algorithms such as LIME [[6]](#references), SHAP [[7]](#references) or counterfactual explanations [[8]](#references). I am reading about novel Bayesian approaches for hyperparameter tuning using Gaussian processes, which is to me more elegant than a classic grid based cross-validation as coded in [`skicit-optimize`](https://scikit-optimize.github.io/stable/). I am curious about novel advances in natural language processing based on transformers and how they are used in large language models such as GPT [[9]](#references) to generate text or BERT [[10]](#references) to encode text. Novel advances in computer vision are also exciting, such as diffusion models [[11]](#references) for image generation. In fact, I find really fascinating how these fields are now overlapping, for example with Stable Diffusion model relying on prompt conditioning using natural language processing, or another example with how transformers can also be used directly for image classification instead of classic convolutional architectures [[12]](#references). Overall, I am aware that things move very fast and assimilating them little by little helps me to integrate them into my daily work at Amazon.

## Master's Thesis on a novel approach for changepoint detection

### The changepoint detection problem

During the summer term at Imperial, I conducted my Master's Thesis research project focusing on online changepoint detection and supervised by [Dr Dean Bodenham](https://www.imperial.ac.uk/people/dean.bodenham) within the [Statistics section](https://www.imperial.ac.uk/statistics/) at Department of Mathematics. In a nutshell, changepoint detection refers to the problem of identifying times at which properties of a time series change. This well-known problem in statistical analysis has applications in a wide range of fields such as health monitoring, cybersecurity, finance or climate. Offline changepoint detection aims to detect changepoints retrospectively in the past, whereas online changepoint detection is expected to detect changepoints sequentially and as fast as possible. Some algorithms are parametric in the sense that they make assumptions on the sampling distribution, whereas other methods are nonparametric.

### Novel approach, package and publication

In this thesis, we review state-of-the-art parametric and nonparametric streaming changepoint detection algorithms [[13-16]](#references) as well as a new approach based on sequentially learning neural networks [[17]](#references). While some reviewed methods do have extensions to multivariate data streams, many do not. We propose a novel approach [[18]](#references) to detecting changepoints in multivariate data streams containing changes in sampling distribution and propose a default deep learning convolutional architecture that does not require any pre-training or fine-tuning. We also introduce a modified version of EWMA [[14]](#references) algorithm to be used along with the neural network in order to detect changepoints in an online manner. Overall, our contribution shows that we can summarise a multivariate changepoint detection problem into a univariate bump detection problem. We compare it with well-known methods on synthetic datasets and also apply it to real world data streams. The proposed method is shown to successfully detect changepoints in simulated and real-world data, as well as in univariate and multivariate time series. I am currently writing a paper to summarise theoritical foundations and results of this new approach on images (computer vision) or text data (natural language processing), where classic methods would not be as efficient due to the complexity and dimensionality of the inputs. In the same time, I developed and published an open-source Python package, [`ocpdet`](https://github.com/vkhamesi/ocpdet), to make them easily accessible and reproducible. Indeed, I believe software development is just as important as theory in research, as it allows more people to benefit from novelty.

## Working as a scientist at Amazon

In November 2022, I joined Amazon in Edinburgh as a Data Scientist to work on machine learning and targeting for online advertising as my first job. In a big picture, my work and research at Amazon focuses on extracting useful contextual information and representations of users in order to predict their interests. I therefore work on a wide range of problems such as representation learning, statistical modeling and experimentation. This is very challenging and exciting since it requires innovative solutions to use the minimal amount of user data. I am learning a lot every day on representation learning architectures, language models and even how to productionise machine learning models to do real time inference at Amazon scale.

# References

[1] Karl Pearson. 1901. [_On lines and planes of closest fit to systems of points in space_](http://www.stats.org.uk/pca/Pearson1901.pdf). Philosophical Magazine.

[2] Teuvo Kohonen. 1982. [_Self-organized formation of topologically correct feature maps_](https://link.springer.com/article/10.1007/BF00337288). Biological Cybernetics.

[3] Harald Lohre et al.. 2020. [_Hierarchical Risk Parity: Accounting for Tail Dependencies in Multi-Asset Multi-Factor Allocations_](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3513399). Machine Learning and Asset Management.

[4] Richard E. Bellman. 2010. [_Dynamic Programming_](https://gwern.net/doc/statistics/decision/1957-bellman-dynamicprogramming.pdf). Princeton Landmarks in Mathematics and Physics.

[5] Victor Khamesi et al.. 2020. [_Quantitative Management of Fund of Funds using Machine Learning_](https://catalogue-bibli.ec-lyon.fr/cgi-bin/koha/opac-detail.pl?biblionumber=126295). École Centrale de Lyon.

[6] Marco Tulio Ribeiro et al.. 2016. [_"Why Should I Trust You?": Explaining the Predictions of Any Classifier_](https://arxiv.org/abs/1602.04938). ACM.

[7] Scott M. Lundberg and Su-In Lee. 2017. [_A Unified Approach to Interpreting Model Predictions_](https://proceedings.neurips.cc/paper_files/paper/2017/hash/8a20a8621978632d76c43dfd28b67767-Abstract.html). NeurIPS.

[8] Riccardo Guidotti. 2022. [_Counterfactual explanations and how to find them: literature review and benchmarking_](https://link.springer.com/article/10.1007/s10618-022-00831-6). Data Mining and Knowledge Discovery.

[9] Alec Radford et al.. 2019. [_Language Models are Unsupervised Multitask Learners_](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf).

[10] Riccardo Guidotti. 2022. [_BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding_](https://arxiv.org/abs/1810.04805). arXiv.

[11] Robin Rombach et al.. 2021. [_High-Resolution Image Synthesis with Latent Diffusion Models_](https://arxiv.org/abs/2112.10752). arXiv.

[12] Alexey Dosovitskiy et al.. 2021. [_An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale_](https://arxiv.org/abs/2010.11929). CVPR.

[13] Ewan Page. 1954. [_Continuous Inspection Schemes_](https://academic.oup.com/biomet/article-abstract/41/1-2/100/456627?redirectedFrom=fulltext). Biometrika.

[14] S. W. Roberts. 1959. [_Control Chart Tests Based on Geometric Moving Averages_](https://www.tandfonline.com/doi/abs/10.1080/00401706.1959.10489860). Technometrics.

[15] Ryan Adams and David MacKay. 2007. [_Bayesian Online Changepoint Detection_](https://arxiv.org/pdf/0710.3742.pdf). arXiv.

[16] Gordon Ross. 2015. [_Parametric and Nonparametric Sequential Change Detection in R: The cpm Package_](https://www.jstatsoft.org/article/view/v066i03). Journal of Statistical Software.

[17] Hushchyn et al.. 2020. [_Online Neural Networks for Change-Point Detection_](https://arxiv.org/abs/2010.01388). arXiv.

[18] Victor Khamesi. 2022. [_ocpdet: A Python package for online changepoint detection in univariate and multivariate data_](https://zenodo.org/record/7632721). Zenodo.
