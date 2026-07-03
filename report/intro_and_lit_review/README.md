

The table below outlines the current state-of-the-art (SOTA) in plant disease classification, tracing the transition from standard CNNs to localized Graph Neural Networks, and highlighting where AgriHGT builds upon existing limitations.

| # | Reference | Year | Dataset | Architecture / Model | Accuracy / Metric | Key Structural Limitation |
| --- | --- | --- | --- | --- | --- | --- |
| **1** | **Hu et al. (HGT)** | **2020** | **Open Academic Graph** | **Heterogeneous Graph Transformer** | **9–21% gain over GNNs** | **Foundational architecture; not designed for or applied to agriculture.** |
| 2 | Srivastava et al. | 2021 | PlantVillage | CNN + Image-Pipeline | 94.87% | Per-image classification only; no cross-crop/disease modelling. |
| 3 | Ferentinos | 2018 | PlantVillage | Deep CNNs (AlexNet, VGG) | 99.53% | Isolated visual reasoning; lacks relational cross-disease tracking. |
| 4 | Murugavalli & Gopi | 2025 | PlantVillage | PLA-ViT (Vision Transformer) | 94.2% | Global visual attention only; no symptom-similarity modeling. |
| 5 | Boukabouya et al. | 2022 | PlantVillage (Tomato) | Vision Transformer | Up to 99.7% | Single-crop scope; lacks relational or graph-based structures. |
| 6 | Liu & Zhang | 2025 | PlantDoc | Efficient Swin Transformer | P: 80.14%, R: 76.27% | Strong global features but no categorical/disease-relation tracking. |
| 7 | Parez et al. | 2023 | Multi-Dataset Composite | GreenViT (Vision Transformer) | 100% / 98% / 99% | Sequential patch attention; lacks cross-crop cross-referencing. |
| 8 | Shandilya et al. | 2025 | Kaggle, Mendeley, CD&S | Hybrid CNN-ViT | 99.15% (Maize) | Single-crop (maize) scope; lacks graph-based cross-crop tracking. |
| 9 | Singha Roy & Kukreja | 2025 | Custom Rice Dataset | Shared Backbone ViT | Disease F1: 54.17% | Single-crop scope; lower accuracy under diverse real-world states. |
| 10 | Ananthajothi & Lokesh | 2026 | Custom Dataset | Graph Neural Network | *Not stated in abstract* | Image-level graphs only; limited disease coverage, no cross-crop links. |
| 11 | Elumalai et al. | 2026 | Spinach & Curry Leaf Set | AE-GNN (Attention GNN) | *Not stated in abstract* | Homogeneous, within-leaf graphs; restricted to two species. |
| 12 | Bera et al. | 2024 | Banana, Potato, PlantDoc | PND-Net (CNN + GCN) | 84.30%–96.18% | Region-pooling graph confined within single individual images. |
| 13 | Bajpai et al. | 2024 | Potato Leaf Dataset | GNN + ResNet18 Fusion | 97.9% (F1: 0.95) | Single-crop (potato) scope; no cross-crop structural sharing. |
| 14 | Maheswara Rao et al. | 2024 | Kaggle (8 Crops) | CNN + GCN Hybrid | *Not stated in abstract* | Standalone CNN/GCN branches per crop; topology is not shared. |
| 15 | Surekha & Subha | 2026 | PlantVillage Subset | AdjLeafGNN (CNN + GNN) | 98.88% (F1: 98.71%) | Models spatial adjacency of leaves, not cross-crop taxonomy. |
| 16 | Li et al. (MARBC) | 2025 | Chinese Rice Text Corpus | RoBERTa-BiLSTM + KG | 94.44% F1 | Text-derived knowledge graph; lacks pixel-level image integration. |
| 17 | Zhao et al. | 2024 | *E. angustifolia* Dataset | LLM + Ag-KG + GAT | 93% | Single-crop scope; knowledge base does not span multi-hosts. |
| 18 | Lin et al. | 2023 | Cassava, IP102, etc. | GPA-Net (Pyramid GNN) | 99% / 97% / 56.9% | Relationships confined to spatial regions *within* an image. |
| 19 | Kalpana et al. | 2025 | PlantVillage | U-Net + Swin-V2 + CoAtNet | 99.31% | High computational complexity; lacks explicit relational tracking. |

