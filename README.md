# Awesome Single-Cell JEPA Models

A curated list of research papers on **Joint-Embedding Predictive Architectures (JEPAs)** for single-cell and spatial omics.

## Contents

- [Single-cell omics](#single-cell-omics)
- [Spatial omics](#spatial-omics)
- [Contributing](#contributing)

**Scope.** Papers must apply a JEPA or a JEPA-inspired latent prediction objective to single-cell or spatial omics data. Hybrid methods qualify when latent prediction is part of the training objective. Papers are grouped by the omics data they model.

**Resources.** Code and checkpoints are checked separately. **Not open-sourced** indicates that no official public implementation was found. **No public checkpoint found** indicates that model weights could not be located in an official release. Resource links were checked on 16 November 2026.

## Single-cell omics

| Model | Paper · Year · Venue | Latent target and context | Code | Checkpoints |
| --- | --- | --- | --- | --- |
| **DCAF** | [Unifying Data Validity, Evaluation Validity and Predictive Modeling for Single-cell Perturbation Simulation](https://doi.org/10.64898/2026.10.13.758713) · Xia et al. · 2026, bioRxiv | Combines JEPA with explicit regulatory dynamics to predict single-cell expression responses to perturbations. | **Not open-sourced** | No public checkpoint found |
| **JEPA-Anything** | [Learning Predictive Models across Different Worlds](https://arxiv.org/abs/2609.20800) · Cui et al. · 2026, arXiv | The single-cell experiments predict complete cell embeddings from masked scRNA-seq and latent perturbation responses from control states and perturbation inputs. | [Project code](https://github.com/Gen-Verse/JEPA-Anything) · [Norman inference code](https://huggingface.co/datasets/Gen-Verse/jepa-anything/blob/main/02_Single_Cell/Norman_Single_Cell_Perturbation_Prediction/test/Norman_Single_Cell_Perturbation_Prediction_test.py) | [Norman checkpoint](https://huggingface.co/datasets/Gen-Verse/jepa-anything/tree/main/02_Single_Cell/Norman_Single_Cell_Perturbation_Prediction/checkpoints) |
| **GB-JEPA** | [Graph-structured joint-embedding prediction for single-cell transcriptomics](https://arxiv.org/abs/2608.05928v2) · Wang et al. · 2026, arXiv | Predicts teacher embeddings pooled over masked, graph-connected gene blocks from the remaining genes in a cell. The first version used the name BioM-JEPA. | **Not open-sourced** · Release announced | No public checkpoint found · Release announced |
| **CellOS** | [Learning a World Model of Cellular State through Joint Embedding Prediction](https://doi.org/10.64898/2026.06.18.733163) · Zhou et al. · 2026, bioRxiv | Uses LLM-JEPA to predict the latent embedding of a perception-ranked transcriptome view from the expression-ranked view of the same cell. | **Not open-sourced** | No public checkpoint found |
| **scJEPA** | [Dual-Space Self-Supervised Learning for Single-Cell Representations](https://openreview.net/pdf?id=KadCjvcLOz) · Zhai et al. · 2026, ICLR LMRL Workshop | Matches cell embeddings across masked and unmasked scRNA-seq views. Training also uses expression denoising and SIGReg. | **Not open-sourced** | [scJEPA checkpoint](https://huggingface.co/zhaiyuyao/scJEPA/tree/main) |
| **Cell-JEPA** | [Latent Representation Learning for Single-Cell Transcriptomics](https://arxiv.org/abs/2602.02093) · ElSheikh et al. · 2026, arXiv | Predicts the unmasked EMA teacher's whole-cell embedding from masked scRNA-seq and also reconstructs masked gene-expression values. | **Not open-sourced** | No public checkpoint found |
| **GeneJEPA** | [A Predictive World Model of the Transcriptome](https://doi.org/10.1101/2025.10.14.682378) · Litman et al. · 2025, bioRxiv | Predicts latent representations of masked gene sets from visible scRNA-seq genes using a Perceiver-style encoder. | [Public training and inference code](https://github.com/BiostateAI/GeneJEPA) · License unspecified in the code repository | [GeneJEPA checkpoint](https://huggingface.co/elonlit/GeneJEPA) |

## Spatial omics

| Model | Paper · Year · Venue | Latent target and context | Code | Checkpoints |
| --- | --- | --- | --- | --- |
| **CellWorld** | [From Gene-Level Reconstruction to Latent Cell Prediction in Spatial Transcriptomics Foundation Models](https://arxiv.org/abs/2608.06659) · Liu et al. · 2026, arXiv | Predicts embeddings of masked cells from visible neighboring cells, target coordinates, and a small partial-expression hint. | [Training and inference code](https://github.com/UoM-HealthAI/CellWorld) | [CellWorld checkpoints](https://huggingface.co/Haiping-UoM/CellWorld) · Authorization required |
| **TERRA** | [Multi-scale modeling of human tissues from spatial transcriptomics with TERRA](https://doi.org/10.64898/2026.07.29.741565) · Birk et al. · 2026, bioRxiv | Predicts masked gene-token embeddings using the focal cell and its spatial neighbors. The encoder produces gene, cell, and neighborhood representations. | [TERRA code](https://github.com/Lotfollahi-lab/terra) | [TERRA-112M inference weights](https://huggingface.co/lotfollahi-lab/TERRA-112M) |
| **SpatialJEPA** | [JEPA-inspired graph-context distillation for spatially aware multiomics integration](https://doi.org/10.64898/2026.07.21.739810) · Mann-Krzisnik & Li · 2026, bioRxiv | Distills cell embeddings from a spatial graph teacher into a student that sees each cell without its neighbors. The student can embed dissociated RNA–ATAC profiles. | [Training and analysis code](https://github.com/li-lab-mcgill/SpatialJEPA) | [Author-listed Zenodo deposit](https://doi.org/10.5281/zenodo.23933515) |
| **ST-JEPA** | [Joint-Embedding Predictive Architecture for Spatial Transcriptomics](https://openreview.net/pdf/d7c8c0703f68e025ff7ce18da069db6da43234b0.pdf) · Birk et al. · 2026, ICML Workshop on Generative and Agentic AI for Biology | Predicts masked gene-token embeddings in spatial cell graphs. Its tokenization supports gene, cell, and neighborhood representations. | **Not open-sourced** | No public checkpoint found |

## Contributing

Suggest a paper or report a broken link by [opening an issue](https://github.com/CHENyiru3/Awesome-single-cell-JEPA-model/issues/new) or opening a pull request. Use the row below for new entries. Describe the context the model sees and the embedding it predicts or matches. Link to the published paper when available and record code and checkpoint availability separately. Place each paper once in the most relevant section.

```markdown
| **Model** | [Paper title](paper-url) · First author et al. · Year, Venue | Context and latent target. | [Official code](code-url) or **Not open-sourced** | [Official checkpoint](checkpoint-url) or No public checkpoint found |
```
