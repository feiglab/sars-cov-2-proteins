# SARS-Cov-2 protein structure models
We have predicted and/or refined SARS-Cov-2 protein structure models. We especially focused on proteins which were hard to predict by using homology modeling (template-based modeling) because of the lack of experimentally determined homolog protein structures. We are publishing two sets of structure models: models based on our structure prediction pipeline and refined AlphaFold models.   

**For detailed modeling procedures and analyses, see [our bioRxiv paper](https://www.biorxiv.org/content/10.1101/2020.03.25.008904v1).**

### Our structure prediction pipeline-based models (FeigLab)
We predicted 10 models for SARS-Cov-2 proteins based on our latest structure prediction pipeline. Our structure prediction pipeline consists of two major features: initial contact-based structure prediction followed by molecular dynamics (MD) simulation-based refinement. We use trRosetta [1] for the initial contact-based structure prediction. We generated 10 models for each target protein, and the best scored model was subjected to the further refinement. Our refinement protocol is based on molecular dynamics (MD) simulations [2]. Various structures are sampled in the vicinity of the initial model structure via MD simulations during the refinement, and a set of low energy conformations is selected and averaged to get an ensemble averaged structure. Our refinement protocol demonstrated success during the last several CASPs with consistent improvements in model qualities. [3] The refinement protocol used here is improved from the method used during the last CASP.

### Refined AlphaFold models (AlphaFold)
Early in March 2020, Google DeepMind published their predicted models on [their web page](https://deepmind.com/research/open-source/computational-predictions-of-protein-structures-associated-with-COVID-19) by using their latest AlphaFold method [4]. The models cover 6 SARS-Cov-2 proteins. We refined those AlphaFold models by using our latest refinement protocol. We found earlier that AlphaFold models which are machine learning-based can be improved further with physics-based refinement method. [5] Physics-based refinement can complement machine learning-based models by providing more atomistic details such as better structure packing and loop structures. We therefore expect that these refined models have increased accuracy over the initial AlphaFold predictions and may be more suitable for further applications such as molecular docking and virtual screening.

### Refined RaptorX models
As a collaboration with Jinbo Xu, we refined his models, which are based on [RaptorX-Contact](http://raptorx.uchicago.edu/), one of the best protein inter-residue contact prediction methods. The models covers the exactly same SARS-CoV-2 proteins that of ours. We applied the same refinement method used for refining AlphaFold models or our in-house structure prediction pipeline.

### Model summary and comparisons
| Protein | RefSeq | FeigLab</br>RaptorX | AlphaFold | Structure difference [A] | Structure change</br>after refinement</br> (AlphaFold) [A] |
|---------|--------|:---------:|:-----------:|:----------------------:|:--:|
|nsp2| [YP_009725298.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725298.1) | 1-638 | 1-345, 438-638 | 15.8 (1-345)</br> 17.1 (438-638) | 1.5 (1-345)</br> 1.9 (438-638) |
|nsp4| [YP_009725300.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725300.1) | 1-500 | 1-489 | 36.3 (1-489)</br> 25.2 (1-273)</br> 8.1 (274-399)</br> 9.8 (400-489)</br> | 1.7 (1-489)</br> 1.8 (1-273)</br> 1.9 (274-399)</br> 0.8 (400-489) |
|nsp6| [YP_009725302.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725302.1) | 1-290 | 1-278 | 18.3 | 2.0 |
|PL-PRO| [YP_009725299.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725299.1) | 1260-1945 | 1571-1927 | 12.4 | 1.5 |
|ORF3a| [YP_009724391.1](https://www.ncbi.nlm.nih.gov/protein/YP_009724391.1) | 1-275 | 38-233 | 14.1 | 2.3 |
|M_protein| [YP_009724393.1](https://www.ncbi.nlm.nih.gov/protein/YP_009724393.1) | 1-222 | 11-203 | 11.6 | 1.3 |
|ORF6 | [YP_009724394.1](https://www.ncbi.nlm.nih.gov/protein/YP_009724394.1) | 1-61  | N/A | N/A | N/A |
|ORF8 | [YP_009724396.1](https://www.ncbi.nlm.nih.gov/protein/YP_009724396.1) | 1-121 | N/A | N/A | N/A |
|ORF10| [YP_009725255.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725255.1) | 1-38  | N/A | N/A | N/A |
|ORF7b| [YP_009725296.1](https://www.ncbi.nlm.nih.gov/protein/YP_009725296.1) | 1-43  | N/A | N/A | N/A |

### Figures of the models
![nsp2](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/nsp2.png)
![nsp4](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/nsp4.png)
![nsp6](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/nsp6.png)
![PL-PRO](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/PL-PRO.png)
![ORF3a](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/ORF3a2.png)
![M_protein](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/M_protein.png)
![Etc](https://github.com/feiglab/sars-cov-2-proteins/blob/master/images/etc.png)

### References
1. Yang, J. *et al.*, Improved protein structure prediction using predicted interresidue orientations, *Proc. Natl. Acad. Sci. USA*, (**2020**). [[LINK]](https://www.pnas.org/content/117/3/1496.short)
2. Heo, L. and Feig, M., PREFMD: a web server for protein structure refinement via molecular dynamics simulations, *Bioinformatics*, (**2017**). [[LINK]](https://academic.oup.com/bioinformatics/article/34/6/1063/4604595)
3. Heo, L, Arbour, C.F., and Feig, M., Driven to near-experimental accuracy by refinement via molecular dynamics simulations, *Proteins* (**2019**). [[LINK]](https://onlinelibrary.wiley.com/doi/full/10.1002/prot.25759)
4. Jumper, J. *et al.*, Computational predictions of protein structures associated with COVID-19, [DeepMind website](https://deepmind.com/research/open-source/computational-predictions-of-protein-structures-associated-with-COVID-19), (March 5, 2020).
5. Heo, L. and Feig, M., High-accuracy protein structures by combining machine-learning with physics-based refinement, *Proteins* (**2019**). [[LINK]](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.25847)
