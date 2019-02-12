.. _PythonAnaconda:

Using the Anaconda Python Distribution
======================================

In this example, we'll show how to use the `Anaconda Python distribution <https://www.anaconda.com/distribution/>`_
on the Rice HPC systems. Anaconda includes many of the commonly used
packages in scientific computing and data science including `Numpy <http://www.numpy.org/>`_
for array computation and `scikit-learn <https://scikit-learn.org>`_
for machine learning.

Let's say we want to run the following script which trains a random
forest classifier on some sample data.

.. literalinclude:: ../../rice-hpc-examples/sklearn-example.py
   :language: python
   :caption: sklearn-example.py

We have our Python script, but we still need to tell the SLURM
scheduler how to run it.

.. literalinclude:: ../../rice-hpc-examples/python-anaconda.slurm
   :language: bash
   :caption: python-anaconda.slurm

The ``module load`` command modifies the current "environment" so that
the Anaconda version of Python is loaded instead of the system Python.

Finally, to submit this to the scheduler, run

.. code-block:: bash

   sbatch python-anaconda.slurm

The resulting STDOUT file should contain the ouput that we printed
to the screen in the above Python script.

Notice that we use the Anaconda Python rather than the default
system Python because we need the scikit-learn package which is
included in the Anaconda distribution. If you need to install any
custom packages, see the :ref:`AnacondaInstall` example.
