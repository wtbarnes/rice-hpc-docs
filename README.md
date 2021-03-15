# This repository is out of date and no longer maintained. Please visit https://researchcomputing.rice.edu/ for documentation regarding documentation for CRC and HPC resources at Rice University.

# Rice CRC Documentation

Documentation for the CRC and HPC Resources at Rice University. The documentation is written in [reStructuredText](http://docutils.sourceforge.net/rst.html) format
and rendered to HTML using the [Sphinx](http://www.sphinx-doc.org) documentation engine.

## Install and Build

To install the needed dependencies using the [Anaconda Python distribution](https://www.anaconda.com/distribution/), run
```shell
> conda env create -f environment.yml
> source activate hpc-docs
```
inside this repository. Alternatively, download all of the packages in [environment.yml](environment.yml) using `pip`.
Then, build the HTML documentation using
```shell
> make html
```
The documentation homepage will be in `_build/html/index.html`.

## Helpful Links

Here are some other resources and examples of nicely formatted HPC documentation:

* [Sheffield HPC Docs](http://docs.hpc.shef.ac.uk/en/latest/hpc/index.html)
* [UiT HPC Docs](https://hpc-uit.readthedocs.io/en/latest/)
* [Python for HPC Help](https://betterscientificsoftware.github.io/python-for-hpc/tutorials/python.doc-sphinx.html)
