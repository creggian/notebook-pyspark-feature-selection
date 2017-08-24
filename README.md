# Pyspark feature selection notebooks

## Introduction

This is a collection of python notebooks showing how to perform feature selection algorithms using Apache Spark. The objective is to provide step-by-step tutorial of increasing difficulty in the design of the distributed algorithm and in the implementation.

## Setup

These notebooks have been built using Python v2.7.13, Apache Spark v2.2.0 and Jupyter v4.3.0. Python and Jupyter come from the Anaconda distribution v4.4.0. Here below there is the script used to launch the jupyter notebook with Pyspark

    #!/bin/bash
    
    export PYSPARK_DRIVER_PYTHON="$ANACONDA2_HOME/bin/jupyter"
    export PYSPARK_DRIVER_PYTHON_OPTS="notebook --NotebookApp.port=8999 --NotebookApp.notebook_dir=$HOME/github/notebook-pyspark-feature-selection"
    export PYSPARK_PYTHON="$ANACONDA2_HOME/bin/python"
    
    $SPARK_HOME/bin/pyspark --master local[4]

## Installation

    git clone git@github.com:creggian/notebook-pyspark-feature-selection.git

## Notebooks

Available notebooks

- [nb-fs-topn.ipynb]: the notebook performs the distributed calculations of the Pearson correlation coefficients matrix between the class vector and the features. It then performs locally the selection of the _top n_ features according to the scores.
- [nb-fs-mrmr.ipynb]: the notebook performs the distributed calculations of the mutual information matrix of class-feature pairs and feature-feature pairs. It then performs locally the mRMR algorithm.
