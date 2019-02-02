Submitting a Job Array
======================

Often you may want to run the same job for a range of different input
parameters. For a large number of different inputs, it is imporactical
to manually submit a job for each unique input. In this case, you may
want to use a job array.

Job arrays are a feature of the SLURM scheduler that allow you to submit
a job for a large range of inputs with a single command. You can read
more about them `here <https://slurm.schedmd.com/job_array.html>`_. A
simple example is provided below.

.. literalinclude:: ../../rice-hpc-examples/job-array.slurm
   :language: bash
   :caption: job-array.slurm

To run this script,

.. code-block:: bash

    sbatch --array=0-4 job_array.slurm

This should run five separate jobs and produce five output files,
``slurm-<JOB_ID>_<TASK_ID>.out``, with the output specified in the above
script. Notice that the environment variable ``$SLURM_ARRAY_TASK_ID`` indexes
the list provided at the prompt.
