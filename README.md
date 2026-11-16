# Awesome Single-Cell JEPA Models

A curated list of research papers on **Joint-Embedding Predictive Architectures (JEPAs)** for single-cell and spatial omics.

## Contents

- [Single-cell omics](#single-cell-omics)
- [Spatial omics](#spatial-omics)
- [Contributing](#contributing)

**Scope.** Papers must apply a JEPA or a JEPA-inspired latent prediction objective to single-cell or spatial omics data. Hybrid methods qualify when latent prediction is part of the training objective. Papers are grouped by the data modeled during training.

## Single-cell omics

| Model | Paper | Year · Venue | Latent target and context | Resources |
| --- | --- | --- | --- | --- |
| **scJEPA** | [Dual-Space Self-Supervised Learning for Single-Cell Representations](https://openreview.net/pdf?id=KadCjvcLOz) · Zhai et al. | 2026 · ICLR Workshop on Learning Meaningful Representations of Life | Matches cell embeddings across masked and unmasked scRNA-seq views. Training also uses expression denoising and SIGReg. | [Checkpoint](https://huggingface.co/zhaiyuyao/scJEPA/tree/main) |

## Spatial omics

| Model | Paper | Year · Venue | Latent target and context | Resources |
| --- | --- | --- | --- | --- |
| **SpatialJEPA** | [JEPA-inspired graph-context distillation for spatially aware multiomics integration](https://doi.org/10.64898/2026.07.21.739810) · Mann-Krzisnik & Li | 2026 · bioRxiv preprint | Distills cell embeddings from a spatial graph teacher into a student that sees each cell without its neighbors. The student can embed dissociated RNA–ATAC profiles. | [Code](https://github.com/li-lab-mcgill/SpatialJEPA) |

## Contributing

Suggest a paper or report a broken link by [opening an issue](https://github.com/CHENyiru3/Awesome-single-cell-JEPA-model/issues/new) or opening a pull request. Use the row below for new entries. Describe the context the model sees and the embedding it predicts or matches. Link to the published paper when available and include official code or checkpoints if released. Place each paper once in the most relevant section.

```markdown
| **Model** | [Paper title](paper-url) · First author et al. | Year · Venue | What the model sees and what embedding it predicts or matches. | [Code](code-url) |
```

List structure inspired by [Awesome Foundation Models for Single-Cell](https://github.com/OmicsML/awesome-foundation-model-single-cell-papers).
