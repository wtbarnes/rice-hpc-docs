# Rice CRC Docs
[![Documentation Status](https://readthedocs.org/projects/rice-hpc-docs/badge/?version=latest)](https://rice-hpc-docs.readthedocs.io/en/latest/?badge=latest)

Documentation for the HPC Resources at Rice University. The documentation is written in [reStructuredText]http://docutils.sourceforge.net/rst.html() format
and rendered to HTML using the [Sphinx](http://www.sphinx-doc.org) documentation engine.

## Install and Build

To install the needed dependencies using the [Anaconda Python distribution](https://www.anaconda.com/distribution/), run
```shell
> conda env create -f environment.yml
```
inside this repository. Alternatively, download all of the packages in <environment.yml> using `pip`.
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
