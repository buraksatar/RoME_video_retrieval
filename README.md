# Our Approaches for Text-to-Video Retrieval
This repo provides the pseudocode for the following works.
- RoME: Role-aware Mixture-of-Expert Transformer for Text-to-Video Retrieval, TCSVT'22 (under review)
- The method got 3rd (joint) award in CVPR'22 Epic Kitchen Multi Instanse Retrieval Challenge (coming soon)
- Semantic Role Aware Correlation Transformer for Text-to-Video Retrieval, ICIP'21

# Semantic Role Aware Correlation Transformer for Text-to-Video Retrieval, ICIP'21

### The model

![Model](img/semantic_model.png)

### The results on YouCook2 Validation Set

Text-to-video retrieval comparison with SOTA approaches on YouCook2 validation set. ’Visual Backbone’ only refers to 3D CNNs Features. Our method surpasses the SOTA methods in the first two parameters when without pre-training.

![Result](img/semantic_resultt.png)

### The ablation experiments

Ablation studies on YouCook2 dataset to investigate the contributions of various feature experts at different levels. The same ablation is also done on HGR method [3] since it is a strong baseline. On 2D + 3D visual features setting, when the feature dimension is 4096, concatenation is done on dimension one; otherwise is done on dimension zero. Our model surpasses HGR with the same hierarchical features with a high margin by using cross-modal attention.

![Ablation](img/semantic_ablation.png)