# Training day on scenario-based LCA and prospective LCA: hands-on with `wurst` and `premise`

This repository holds the teaching material for 
the training day on `wurst` and `premise` held on
May the 16th offered by the Sustainable Systems 
Research Group (SSRG) at the University of Toronto.

## Course objectives

The objective of this course is to provide an introduction to the
LCA methodology and the tools used to perform it. The course will
be divided in four parts:

1. Introduction to the [``wurst``](https://github.com/polca/wurst) library.
2. Introduction to the [``premise``](https://github.com/polca/premise) library.
3. Practical session on scenario-based and prospective LCA.
4. If time allows, we will introduce the [``activity-browser``](https://github.com/LCA-ActivityBrowser/activity-browser) library.


## Course description

This course will introduce participants to prospective and scenario-based LCA, 
software to conduct it and large-scale manipulation of LCA databases. Hence, 
the course is divided in three parts. 

The first part will be an introduction to
the ``wurst`` library, which is a python library used to operate
large-scale modification on LCA databases. 

The second part will be
an introduction to the ``premise`` library, which is a python library
used to create and operate prospective LCA database based on IAM
scenarios. 

The third part will be a practical session where the
participants will be able to build their own prospective scenarios
using the ``premise`` library.

The fourth part will be an introduction to the ``activity-browser`` library, 
which is a graphical user interface for `brightway`.

## Contact

In case of questions or issues with the instructions below, please contact:
[Romain Sacchi](mailto:romain.sacchi@psi.ch)

## License

Unless otherwise specified, all material in this repository is licensed [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/legalcode).

## Requirements

No special requirements are needed at the beginning of the course.
It is however best to install the required software before the course.

We ask the participants to download the following Python library managers
before the course:

- Anaconda: https://www.anaconda.com/products/distribution
- Git: https://git-scm.com/downloads

## Instructions

Install the `libmamba` solver in conda, for faster environment resolution.
Open the terminal (Anaconda terminal in Windows) and run the following commands:

```bash
  conda install -n base conda-libmamba-solver
  conda config --set solver libmamba
```

Clone this repository onto your computer by running the following command 
in the terminal:

```bash
  git clone 
```

### Morning session

For the morning part of the course, we will use the `wurst` library.
Hence, we ask the participants to install the `wurst` library and dependencies 
by running the corresponding conda recipe found under `environments/wurst_environment.yaml.

Using the terminal, navigate to the `environments` folder and run the following 
command:

```bash
  mamba env create -f wurst_environment.yaml
```

This will create a conda environment called `wurst` with all the required dependencies.

### Afternoon session

For the afternoon part of the course, we will use the `premise` library.

Using the terminal, navigate to the `environments` folder
and run the following command:

```bash
  mamba env create -f premise_environment.yaml
```