# AgriHGT — Literature Review Summary Table

| # | Ref. | Year | Dataset | Model | Accuracy / Metric | Key Limitation |
|---|------|------|---------|-------|--------------------|-----------------|
| 1 | Hu, Dong, Wang & Sun (HGT) | 2020 | Open Academic Graph (179M nodes, 2B edges) | Heterogeneous Graph Transformer | 9–21% gain over GNN baselines (NDCG/MRR) | Foundational architecture; not designed for or applied to plant disease / agriculture |
| 2 | Srivastava et al. | 2021 | PlantVillage | CNN + image-processing pipeline | 94.87% | Per-image classification only; no cross-crop or cross-disease modelling |
| 3 | Ferentinos | 2018 | PlantVillage | Deep CNN (AlexNet, GoogLeNet, VGG) | 99.53% | Same limitation; no relational reasoning across diseases |
| 4 | Murugavalli & Gopi (PLA-ViT) | 2025 | PlantVillage | Vision Transformer | 94.2% | Global visual attention only; no symptom-similarity or crop-relation modelling |
| 5 | Boukabouya et al. | 2022 | PlantVillage (tomato subset) | Vision Transformer | up to 99.7% | Single-crop scope; no relational or graph-based reasoning |
| 6 | Liu & Zhang | 2025 | PlantDoc | Efficient Swin Transformer | P: 80.14%, R: 76.27% | Strong global features but no disease-relation modelling |
| 7 | Parez et al. (GreenViT) | 2023 | PlantVillage, DRLI, Plant Composite | Vision Transformer | 100% / 98% / 99% | Sequential-patch global attention only; no cross-crop relational modelling |
| 8 | Shandilya et al. | 2025 | Kaggle + Mendeley maize; CD&S | Hybrid CNN-ViT | 99.15% (99.13% F1); 95.93% on CD&S | Single-crop (maize) scope; no graph-based or cross-crop reasoning |
| 9 | Singha Roy & Kukreja | 2025 | Custom rice-leaf dataset (3,345 images) | Vision Transformer (shared backbone) | Disease F1: 54.17%; Severity F1: 77.94% | Single-crop scope; moderate accuracy; no relational modelling |
| 10 | Ananthajothi & Lokesh | 2026 | Custom plant image dataset (4 diseases) | Graph Neural Network | — | Image-level graphs only; limited disease coverage, no cross-crop links |
| 11 | Elumalai, Annamalai & Devika M | 2026 | Curated half-spinach & curry-leaf set (15 diseases) | Attention-Enhanced GNN (AE-GNN) | — | Homogeneous, within-leaf graphs; restricted to two species |
| 12 | Bera et al. (PND-Net) | 2024 | Banana, CoLeaf, Potato, PlantDoc | CNN + Graph Convolutional Network | 84.30%–96.18% | Region-pooling graph built within single images; no cross-crop disease-relation modelling |
| 13 | Bajpai et al. | 2024 | Potato leaf disease dataset | GNN + ResNet18 fusion | — | Single-crop (potato) scope; no cross-crop relational tracking |
| 14 | Maheswara Rao et al. | 2024 | Kaggle (31 classes, 8 crops) | CNN + Graph Convolutional Network | — | Per-crop standalone CNN/GCN branches; graph structure not shared across crops |
| 15 | Surekha & Subha Mastan Rao (AdjLeafGNN) | 2026 | PlantVillage subset | LDDNet (CNN) + GNN | 98.88% (98.71% F1) | Graph models adjacency between leaves of the same crop, not relations across crops |
| 16 | Li et al. (MARBC) | 2025 | Chinese rice disease/pest text corpus | RoBERTa-BiLSTM-CRF + Knowledge Graph | 94.44% F1 | Text-derived knowledge graph for a single crop; no image-based cross-crop reasoning |
| 17 | Zhao et al. | 2024 | *Elaeagnus angustifolia* disease dataset | LLM + Agricultural KG + Graph Attention Network | 93% | Single-crop scope; knowledge graph not extended across host plants |
| 18 | Lin et al. (GPA-Net) | 2023 | Cassava Leaf, AI Challenger, IP102 | Graph Pyramid Attention CNN | 99% / 97% / 56.9% | Graph relations confined to spatial regions within an image, not across crops |
| 19 | Kalpana et al. | 2025 | PlantVillage | U-Net + Swin-V2 segmentation; CoAtNet + Enhanced CoAtNet (LFHBA fusion) | 99.31% (P: 99.32%, F1: 99.31%) | High structural/computational complexity; no cross-crop relational tracking |

---

**Summary:** Across all 18 plant-disease studies (rows 2–19), every method treats disease classification as an independent, per-image (or per-crop) decision. Where relational structure exists at all (rows 10–18), it is confined to a single image, a single crop, or one-to-two species — never spanning multiple unrelated host plants. AgriHGT (row 1's architecture, adapted) is positioned to close this gap by modelling crop, disease, and image-feature nodes jointly in one heterogeneous graph.
