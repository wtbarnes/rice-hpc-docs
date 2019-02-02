A Simple SLURM Example
======================

In this example, we'll create a simple SLURM script that prints "Hello World!"
to STDOUT. First, create a script called ``hello-world.slurm``.

.. literalinclude:: ../../rice-hpc-examples/hello-world.slurm
   :language: bash
   :caption: hello-world.slurm

This defines what our task is (printing "Hello World!") and how the cluster
should run it. Note that we've given our job a name (``hello-world``) and
told it run in the ``commons`` queue with a maximum execution time of one
minute. We won't worry about the other options for now.

To submit this script to SLURM (the job scheduler),

.. code-block:: bash

   sbatch hello-world.slurm

If the job was successfully submitted, you should see
``Submitted batch job <JOB_ID>``,where ``JOB_ID`` is the ID assigned to your
job by the scheduler. When the jobfinishes, you should see the file
``slurm-<JOB_ID>.out`` in the directory you submitted the job from and it
should contain the text ``Hello World!``.
