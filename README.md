# Robustness

Repo containing utilities for robustness analysis of Deep Neural Networks such as the creation of image distortions, weight perturbations, and Out-Of-Distribution (OOD) datasets.

## Dataset
Download the dataset from the link embedded in the name. Datasets with * can be automatically downloaded.
| Dataset | Type | Train Size | Test Size | #Classes |
|:-:|:-:|:-:|:-:|:-:|
| [CIFAR-10-C](https://github.com/hendrycks/robustness) | OOD| 50,000 | 10,000 | 10 |
| [CIFAR-100-C](https://github.com/hendrycks/robustness) | | 50,000 | 10,000 | 100 |

- The OOD datasets are perturbed versions of the IID counterparts. 15 types of distortions are available (e.g., Gaussian Noise and Impulse Noise) with different levels of intensity (from 1 to 5). The code for the creation of these datasets is available in the `utility/ood_dataset.py`. Since these datasets are available only with 32x32 resolution, we provide the code for evaluating the distortions at any resolution in `evaluate_cifar10c.py`.

# References
[1] FlatNAS: optimizing Flatness in Neural Architecture Search for Out-of-Distribution Robustness [ACCEPTED WCCI 2024] (https://arxiv.org/abs/2402.19102)

[2] Benchmarking Neural Network Robustness to Common Corruptions and Perturbations, ICLR 2019 (https://openreview.net/forum?id=HJz6tiCqYm)
