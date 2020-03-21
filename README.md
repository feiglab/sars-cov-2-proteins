# SARS-Cov-2 protein structure models
We have predicted and/or refined SARS-Cov-2 protein structure models. We especially focused on proteins which were hard to predict by using homology modeling (template-based modeling) because of the lack of experimentally determined homolog protein structures. We published two sets of structure models: models based on our structure prediction pipeline and refined AlphaFold models.   

### Our structure prediction pipeline-based models (FeigLab)
We predicted 10 models for SARS-Cov-2 proteins based on our latest structure prediction pipeline. Our structure prediction pipeline is consist of two major features: initial contact-based structure prediction and followed molecular dynamics (MD) simulation-based refinement. We use [trRosetta](https://www.pnas.org/content/117/3/1496) [1] for the initial contact-based structure prediction. We generated 10 models for each target protein, and the best scored model was subjected to the further refinement. Our refinement protocol is based on molecular dynamics (MD) simulations [2]. Various structures are sampled in the vicinity of the initial model structure via MD simulations during the refinement, and a set of low energy conformations is selected and averaged to get an ensemble averaged structure. The refinement protocol have shown successes during the last several CASPs with consistent improvements of model qualities. [3] The applied refinement protocol has been significantly improved from the method used during the last CASP.

### Refined AlphaFold models (AlphaFold)
Early in March, 2020, Google DeepMind published their predicted models on [their web page](https://deepmind.com/research/open-source/computational-predictions-of-protein-structures-associated-with-COVID-19) by using their latest AlphaFold method [4]. The models covers 6 SARS-Cov-2 proteins, which are overlapped to ours. We examined earlier that AlphaFold models which are machine learning-based can be improved further with physics-based refinement method. [5] Physics-based refinement can complement machine learning-based models by providing more atomistic details such as better structure packing and loop structures. 

### Model summary


### References
1. Yang, J. *et al.*, Improved protein structure prediction using predicted interresidue orientations, *Proc. Natl. Acad. Sci. USA*, (**2020**). [[LINK]](https://www.pnas.org/content/117/3/1496.short)
2. Heo, L. and Feig, M., PREFMD: a web server for protein structure refinement via molecular dynamics simulations, *Bioinformatics*, (**2017**). [[LINK]](https://academic.oup.com/bioinformatics/article/34/6/1063/4604595)
3. Heo, L, Arbour, C.F., and Feig, M., Driven to near-experimental accuracy by refinement via molecular dynamics simulations, *Proteins* (**2019**). [[LINK]](https://onlinelibrary.wiley.com/doi/full/10.1002/prot.25759)
4. Jumper, J. *et al.*, Computational predictions of protein structures associated with COVID-19, [DeepMind website](https://deepmind.com/research/open-source/computational-predictions-of-protein-structures-associated-with-COVID-19), (March 5, 2020).
5. Heo, L. and Feig, M., High-accuracy protein structures by combining machine-learning with physics-based refinement, *Proteins* (**2019**). [[LINK]](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25847)
