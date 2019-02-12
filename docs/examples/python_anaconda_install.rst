.. _AnacondaInstall:

Installing Packages with Anaconda
=================================

The :ref:`PythonAnaconda` gives an example of how to run Python script
using the Anaconda Python distribution. Anaconda is also useful if you
need to install a set of custom packages not included in the system
Python or Anaconda in order to run your code on cluster.

In this example, we'll use the `SunPy package <https://sunpy.org/>`_
for data analysis in solar physics to do some coordinate transformations.

.. literalinclude:: ../../rice-hpc-examples/sunpy-example.py
   :language: python
   :caption: sunpy-example.py

However, SunPy is not installed by default so we'll need to use Anaconda
to install it first. We'll do this using an *environment* file. You can
read more about Anaconda environments `here <https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html>`_.

.. literalinclude:: ../../rice-hpc-examples/sunpy-env.yml
   :language: yaml
   :caption: sunpy-env.yml

Before running the script, we need to create the environment and install
the SunPy package and all of the needed dependencies,

.. code-block:: bash

   module load Anaconda3
   conda env create -f sunpy-env.yml

Now that we have the needed packages installed, we need to tell the
scheduler to load Anaconda, load the correct environment, and run the script.

.. literalinclude:: ../../rice-hpc-examples/anaconda-install.slurm
   :language: bash
   :caption: anaconda-install.slurm

Finally, to submit this to the scheduler,

.. code-block:: bash

   sbatch anaconda-install.slurm

The resulting STDOUT file should contain the ouput that we printed
to the screen in the above Python script.
