---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Supplementary Website
---

This website provides the appendix and other supplementary data for the paper "Scaling Interprocedural Static Data-Flow Analysis to Large C/C++ Applications: An Experience Report".

The paper analyzes performance bottlenecks of the *Interprocedural Distributive Environments* (IDE) algorithm and proposes two optimizations to improve runtime and memory consumption of IDE analyses: 
- Improved memory-layouts of the internal data structures of the IDE solver and
- extensions to a garbage collection mechanism for the IDE solver internal data.

The paper contains a thorough empirical study to assess the concrete performance implications of our proposed optimizations, when analyzing real-world C and C++ software.

## IDE Algorithm

We provide a copy of the IDE algorithm [here](algorithm) to help understanding our proposed optimizations.

## Additional Visualizations

We provide additional visualizations of the results of our empirical study.
These can be used to gain additional insoght into the collected data.
You can find these visualizations [here](plots).

## Supplementary Material

The supplementary material contains the raw results from our evaluation, all plots generated from these results, as well as the source code of our implementation.
You can download a zip archive of the supplementary material [here](https://doi.org/10.5281/zenodo.13137082).
