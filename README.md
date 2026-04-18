# vision-transformer-cifar10-review

This repository contains a literature review and scaled-down empirical replication based on the paper **"An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale"** by Dosovitskiy et al. (2021).

## Project summary

The project studies the Vision Transformer (ViT) and compares it with ResNet-20 on CIFAR-10 across different training data fractions: 10%, 25%, 50%, and 100%.

The main goal is to examine the paper's claim that transformer performance depends strongly on data scale. In our small-scale experiment, ResNet-20 outperformed ViT-S/4 across all data fractions, but the performance gap narrowed as more training data was used.

## Repository contents

- `notebooks/` — training and analysis notebook
- `figures/` — plots used in the report
- `results/` — saved JSON outputs from training runs
- `report/` — final mini-project report

## Main results

Best test accuracy on CIFAR-10:

| Training fraction | ViT-S/4 | ResNet-20 |
|---|---:|---:|
| 10% | 0.5661 | 0.7260 |
| 25% | 0.6779 | 0.8134 |
| 50% | 0.7536 | 0.8591 |
| 100% | 0.8116 | 0.8873 |

## Key findings

- ResNet-20 performs better in the low-data regime
- ViT-S/4 improves steadily as more data becomes available
- The gap between the two models narrows with data scale
- Learned positional embeddings recover meaningful spatial structure
- Attention patterns become broadly more global in deeper transformer layers

## Reference

Dosovitskiy, A. et al. (2021). *An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale*.
