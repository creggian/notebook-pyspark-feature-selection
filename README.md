# Pyspark feature selection notebooks

## Setup

These notebooks have been built using Python v2.7.13, Apache Spark v2.2.0 and Jupyter v4.3.0. Python and Jupyter come from the Anaconda distribution v4.4.0. Here below there is the script used to launch the jupyter notebook with Pyspark

    #!/bin/bash
    
    export PYSPARK_DRIVER_PYTHON="$ANACONDA2_HOME/bin/jupyter"
    export PYSPARK_DRIVER_PYTHON_OPTS="notebook --NotebookApp.port=8999 --NotebookApp.notebook_dir=$HOME/github/notebook-pyspark-feature-selection"
    export PYSPARK_PYTHON="$ANACONDA2_HOME/bin/python"
    
    $SPARK_HOME/bin/pyspark --master local[2]
