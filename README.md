# Our Approaches for Text-to-Video Retrieval
This repo provides the pseudocode for the following works.
- RoME: Role-aware Mixture-of-Expert Transformer for Text-to-Video Retrieval, TCSVT'22 (under review)
- The method got 3rd (joint) award in CVPR'22 Epic Kitchen Multi Instanse Retrieval Challenge (coming soon)
- Semantic Role Aware Correlation Transformer for Text-to-Video Retrieval, ICIP'21

# The pseudocode

We follow [HGR](https://github.com/cshizhe/hgr_v2t) method as a baseline.
You may easily replicate our experiments by following the baseline code and our directions.
- For textual encoding, we use semantic role labeling [tool](https://demo.allennlp.org/semantic-role-labeling) from AllenNLP.
- We extract video features by following this [repo](https://github.com/antoine77340/video_feature_extractor).
- We add certain transformer encoder and decoders in the video encoding part, by using [transformers](https://pytorch.org/docs/stable/generated/torch.nn.Transformer.html) from PyTorch.
- Other parts are clearly mentioned in the papers.
- If any question you have, I would be happy to answer them or clarify the things regarding the implemention/paper.

# RoME: Role-aware Mixture-of-Expert Transformer for Text-to-Video Retrieval, TCSVT'22 (under review)

### The model

### The results on YouCook2 Validation Set

### The results on MSR-VTT

# Technical report for the method got 3rd (joint) award in CVPR'22 Epic Kitchen Multi Instanse Retrieval Challenge

(coming soon)

# Semantic Role Aware Correlation Transformer for Text-to-Video Retrieval, ICIP'21

### The model

![Model](img/semantic_model.png)

### The results on YouCook2 Validation Set

Text-to-video retrieval comparison with SOTA approaches on YouCook2 validation set. ’Visual Backbone’ only refers to 3D CNNs Features. Our method surpasses the SOTA methods in the first two parameters when without pre-training.

![Result](img/semantic_resultt.png)

### The ablation experiments

Ablation studies on YouCook2 dataset to investigate the contributions of various feature experts at different levels. The same ablation is also done on HGR method [3] since it is a strong baseline. On 2D + 3D visual features setting, when the feature dimension is 4096, concatenation is done on dimension one; otherwise is done on dimension zero. Our model surpasses HGR with the same hierarchical features with a high margin by using cross-modal attention.

![Ablation](img/semantic_ablation.png)

### References

If you find this any part of this repo useful, we'd really appreciate it if you could cite the following papers
[1] RoME: Role-aware Mixture-of-Expert Transformer for Text-to-Video Retrieval:

```


```

[2] Semantic Role Aware Correlation Transformer For Text To Video Retrieval:

```
@INPROCEEDINGS{9506267,
    author={Satar, Burak and Hongyuan, Zhu and Bresson, Xavier and Lim, Joo Hwee},  
    booktitle={2021 IEEE International Conference on Image Processing (ICIP)},   
    title={Semantic Role Aware Correlation Transformer For Text To Video Retrieval},   
    year={2021},  
    volume={},  
    number={},  
    pages={1334-1338},  
    doi={10.1109/ICIP42928.2021.9506267}
}
```
