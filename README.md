<h1 align="center"><b>awesome-OOD-Graph-CL</b></h1>
<p align="center">
    <a href="https://github.com/kokolerk/awsome-ood-rank/pulls"><img src="https://img.shields.io/badge/PRs-Welcome-green" alt="PRs"></a>
    <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="awesome"></a>
    <a href="https://graph.ood-generalization.com/"><img src="https://img.shields.io/badge/-Website-grey?logo=svelte&logoColor=white" alt="Website"></a>
    <img src="https://img.shields.io/github/stars/kokolerk/awsome-ood-rank?color=yellow&label=Star" alt="Stars" >
    <img src="https://img.shields.io/github/forks/kokolerk/awsome-ood-rank?color=blue&label=Fork" alt="Forks" >
</p>

This repository contains the paper list of 3 fields: **Out-of-Distribution (OOD) Generalization, Out-of-Distribution (OOD) Generalization for graph and contrastive learning**. Although these three fields are distinct, they can potentially intersect with each other from the perspective of feature analysis, i.e. *dimensional collapse*, *neural collapse*, *singuler values distribution*.


We will try our best to make this paper list updated. If you notice some related papers missing, do not hesitate to contact us via pull requests at our repo.

# Contents
- [Papers](#papers)
  - [Contrastive Learning](#contrastive-learning)
      - [Generalized Analysis and Methods](#generalized-analysis-and-methods)
      - [Graph Contrastive Learning](#graph-contrastive-learning)
  - [Out-of-distribution Generalization](#out-of-distribution-generalization)
      - [Generalized Analysis and Methods](#generalized-analysis-and-methods-1)
      - [Specialized for graph](#specialized-for-graph--graph-invariant-learning-)
  - [Other Related Papers](#other-related-papers)
      - [Dataset for Graph OOD](#dataset-for-graph-ood)
  - [Reference blogs](#reference-blogs)

# Papers

## Contrastive Learning

#### Generalized Analysis and Methods
Survery:
- [CVPR 2020] A Survey on Contrastive Self-supervised Learning [[paper]](https://arxiv.org/abs/2011.00362.pdf) several CL losses

Papers (based on dimensional collapse):
- [ICCV 2021 Oral] On Feature Decorrelation in Self-Supervised Learning [[paper]](https://arxiv.org/abs/2105.00470.pdf) definition of dimensional collapse in self-supervised learning.
- [ICLR 2022] Understanding Dimensional Collapse in Contrastive Self-supervised Learning [[paper]](https://arxiv.org/abs/2110.09348.pdf) linear theory through singular value analysis.
- [ICLR 2023] ContraNorm: A Contrastive Learning Perspective on Oversmoothing and Beyond [[paper]](https://arxiv.org/abs/2303.06562.pdf) uniform loss for feature space
- [ICLR 2023] A Message Passing Perspective on Learning Dynamics of Contrastive Learning [[paper]](https://arxiv.org/abs/2303.04435.pdf) CL is graph message passing in positive graph and negtive graph
- Which Features are Learnt by Contrastive Learning? On the Role of Simplicity Bias in Class Collapse and Feature Suppression [[paper]](https://arxiv.org/abs/2305.16536) test set analysis for superviesd and non-supervised CL


#### Graph Contrastive Learning
Survey:
- [arXiv 2021] Graph Self-Supervised Learning: A Survey [[paper]](https://arxiv.org/pdf/2103.00111.pdf) several CL methods in graph 

Papers (based on data augmentaion)：
- [NeurIPS 2020] Graph Contrastive Learning with Augmentations [[paper]](https://arxiv.org/pdf/2010.13902.pdf) emprirical analysis for DA in graph 
- [KDD 2020] GCC: Graph Contrastive Coding for Graph Neural Network Pre-Training [[paper]](https://arxiv.org/pdf/2006.09963.pdf) 
- [ICML 2022] G-Mixup: Graph Data Augmentation for Graph Classification [[paper]](https://arxiv.org/pdf/2202.07179.pdf) Graphon for mixup DA
- [arXiv] On Understanding and Mitigating the Dimensional Collapse of Graph Contrastive Learning:a Non-MaximumRemoval Approach [[paper]](https://arxiv.org/abs/2203.12821.pdf) adapt Understanding Dimensional Collapse in Contrastive Self-supervised Learning in graph





## Out-of-distribution Generalization

#### Generalized Analysis and Methods
Survey:
- [survey] Towards Out-Of-Distribution Generalization: A Survey [[paper]](https://arxiv.org/pdf/2108.13624.pdf)

Papers (based on IRM):
- Invariant Risk Minimization [[paper]](https://arxiv.org/pdf/1907.02893.pdf)
- [ICML 2020] Invariant Rationalization [[paper]](https://arxiv.org/abs/2003.09772.pdf) interesting formulation, invariance + mutual information
- [NeurIPS 2021] Invariance Principle Meets Information Bottleneck for Out-of-Distribution Generalization [[paper]](https://arxiv.org/abs/2106.06607.pdf) 
- [AISTATS 2021] Does Invariant Risk Minimization Capture Invariance? [[paper]](https://arxiv.org/abs/2101.01134.pdf) fairly good paper, analyzing when will IRMv1 fail (to get the solution of IRM), and when will IRM itself fail
- [ICLR 2021] The risks of invariant risk minimization [[paper]](https://arxiv.org/abs/2010.05761.pdf)  IRM failue cases
- [ICML 2021] Out-of-Distribution Generalization via Risk Extrapolation (REx) [[paper]](https://arxiv.org/abs/2003.00688.pdf) generalization of IRM, propose MM-REx and V-REx (use variance among losses from domains as penalty)
- ZIN: When and How to Learn Invariance Without Environment Partition? [[paper]](https://arxiv.org/abs/2203.05818.pdf) case when no environment information proved IRM fails.

#### Specialized for graph ( graph invariant learning )
Survey:
- [survey] Out-Of-Distribution Generalization on Graphs: A Survey [[paper]](https://arxiv.org/pdf/2202.07987.pdf)

Papers (based on invaraint learning):
- [NeurIPS 2022] Learning Invariant Graph Representations for Out-of-Distribution Generalization [[paper]](https://haoyang.li/assets/pdf/2022_NeurIPS_GIL.pdf) DIL, adapt Invariant Rationalization in graph
- [NeurIPS 2022] Learning Causally Invariant Representations for Out-of-Distribution Generalization on Graphs [[paper]](https://arxiv.org/pdf/2202.05441.pdf) CIGA, adapt CL AND Invariant Rationalization for graph
- [NeurIPS 2022] Dynamic Graph Neural Networks Under Spatio-Temporal Distribution Shift [[paper]](https://haoyang.li/assets/pdf/2022_NeurIPS_DIDA.pdf) adapt GNN ood for DGNN graph
- [ICLR 2022] Discovering Invariant Rationales for Graph Neural Networks [[paper]](https://arxiv.org/pdf/2201.12872.pdf) DIR, adapt IRM in graph
- [ICML 2022] Interpretable and Generalizable Graph Learning via Stochastic Attention Mechanism [[paper]](https://arxiv.org/pdf/2201.12987.pdf) adapt edge-level attention to extract subgraph
- [NeurIPS 2023] Does Invariant Graph Learning via Environment Augmentation Learn Invariance? [[paper]](https://arxiv.org/abs/2310.19035.pdf) adapt ZIN in graph with ERM model 



## Other Related Papers

#### Dataset for Graph OOD

- [NeurIPS 2022] GOOD: A Graph Out-of-Distribution Benchmark [[paper]](https://openreview.net/pdf?id=8hHg-zs_p-h)
- [NeurIPS 2021 Workshop] A Closer Look at Distribution Shifts and Out-of-Distribution Generalization on Graphs [[paper]](https://openreview.net/pdf?id=XvgPGWazqRH)
- [arXiv 2022] DrugOOD: Out-of-Distribution (OOD) Dataset Curator and Benchmark for AI-aided Drug Discovery -- A Focus on Affinity Prediction Problems with Noise Annotations [[paper]](https://arxiv.org/pdf/2201.09637.pdf)

## Reference blogs

- OOD generalization related papers (based on IRM) [[blog]](https://sites.google.com/view/mila-ood-rg/related-work)
- OOD generalization paper list (general) [[blog]](https://out-of-distribution-generalization.com/)
- OOD generalization for Graph paper list (general) [[blog]](https://graph.ood-generalization.com/)

