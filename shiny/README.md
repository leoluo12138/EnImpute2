---
title: "README"
author: "Yu-Heng Luo"
date: "2022-11-02"
output:
  html_document: default
  pdf_document: default
editor_options:
  markdown:
    wrap: 72
---

# User guide for EnImpute2' shiny platform

This is a user guide for EnImpute2's shiny platform,supporting the paper
**"EnImpute2: Gene expression recovery for single cell RNA-sequencing
data via ensemble learning"**,where you can find at xxxx.

To start with,you need to download EnImpute2 successfully and set up the
corresponding python environment correctly.Preparatory work can be done
as follows:

```{r eval=FALSE}
library(EnImpute2)
library(reticulate)
use_condaenv(".../anaconda/envs/enimpute2_py37/python.exe")#"enimpute2_py37" is your corresponding python environment
py_config()
```

Overall,the shiny platform is mainly consisted of six
sections------Home,Imputation,Downstream analysis,User guide,Contact us
and Reference.The details of each section's function will be explained
as follows:

## Home

Home section is a welcome page for users.This page possesses the most
basic workflow about EnImpute2. For detailed information about
EnImpute2,please refer to the supplementary paper.

## Imputation

Imputation section is for users to get the EnImpute2 imputation
result.The left panel is for users to upload the matrix which requires
imputation.The format should be .*csv*. Rows represent genes and columns
correspond to cells.

When the imputation is done(usually the process will last an hour or
so),the time used will be shown in the middle panel,and users can
download the EnImpute2 imputation matrix in the right panel.

## Downstream analysis

Downstream analysis is divided into four subsections which correspond to
the four downstream analysis in the paper.Here we mainly present some
visualization results regarding each experiment.This section is divided
into four subsections:

### Recovery gene expression

Users should upload the raw matrix and the imputation matrix in the left
panel.Then click the button"Start Recovery Visualiazation!" to start.
When users click the botton
,UMAP dimensionality reduction visulization of two matrices will be shown on the right side.Users can adjust the number and the type of individual methods to be considered in EnImpute2 by the visualization image.

### Cell clustering

Users should upload the raw matrix and the imputation matrix in the left
panel.Then click the button"Start Cluster Visualization!" to start.After
a minute or so,ARI and NMI of two matrices will be shown on the right side.Users can adjust the number and the type of individual methods to be considered in EnImpute2 by comparing the difference between two pictures.

### Differential analysis

The upload matrices are different here.The uploaded matrices must contain three columns:one is all genes' name,one is log2FC and the other one is pvalue.Then
click the button"Start Differential Visualization!" to start.When the process is finished,volcano plots of two matrices will be shown on the
right panel.
Users can adjust the number and the type of individual methods to be considered in EnImpute2 by the volcano pictures.

### Trajectory analysis

Users should upload the raw matrix and the imputation matrix in the left
panel.Then click the button"Start Trajectory Visualization!" to start.
When the process is done,lineage reconstruction by monocle2 of two
matrices will be shown on the right side.You can adjust
the number and the type of individual methods to be considered in EnImpute2 by the visualization image.

## User guide

The instructions on how to use the platform to implement all the
experiments,which is this page's article.

## Contact us

Information about the author,should you have any questions or
suggestions please do not hesitate to contact us.

## Reference

Reference section lists out all the reference in the paper.
