# Pods Service Performance Analytics Repository

The Tapis Pods Service is an open-source, API which enables researchers to seamlessly manage Kubernetes containers, volumes, networking, and security funded by the National Science Foundation and hosted at the Texas Advanced Computing Center (TACC).

The goal of this repository is to act as a center of operations for experiments with the Pods service. This repository will contain information and code used to create our experiments and graphics. Code will usually be presented in the form of Jupyter Notebooks (.ipynb) and consists of Python code blocks.

## Repository Composition

This repository holds the following folders and files:
 
 **experiments.ipynb**  
This Jupyter Notebook file can be ran with `jupyter experiments.ipynb` or importing the file to your preferred Jupyter client. The notebook contains all the Python code used in experiment initialization along with actual testing. The notebook describes setting up container environments in different experiment cases and processing experiment data.

**graph.ipynb**  
This Jupyter Notebook file contains all the Python code used in parsing our experiment data and visualizing it. The visualization is done with Python's `matplotlib` and `pandas` libraries.
 
**docker-compose.yml**  
This docker-compose file can be ran with `docker-compose up` when starting in this directory. This file describes an environment for docker-compose to create using docker. In this case, a Neo4j database, a Postgres database, and a FastAPI service will be created locally for testing.

**~/experiment_data**  
This folder contains `.csv` files which contain outputs from our experiments. Which experiment and which experiment case is stated in the filenames.

**~/images_and_graphs**  
This folder contains graphics which were created by our `graph.ipynb` notebook for use in our paper. The filenames describe the experiment and experiment case.

**~/initial_synthetic_data**  
This folder contains the initial synthetic data which was used in our different experiment cases. This initial synthetic data was created by Python code which is in our `experiments.ipynb` Jupyter notebook. The filenames describe the experiment case. 

 
## Information
This experiment relies on the Pods service hosted by TACC at `https://tacc.tapis.io/v3/pods`. The experiment also relies on AuraDB and Google Cloud Postgres. All of which should be accessible via free accounts. The local machine testing done was completed on a high-end laptop, but should not greatly affect the outcome. You will have to work around any issues that you might face as your situation will not match ours in the case of you running the experiment yourself.
