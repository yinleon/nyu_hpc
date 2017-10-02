## Slurm Sweeper
#### By Leon Yin <i>Last Updated 2017-10-02</i>
This Python script is to be run on NYU HPC's Prince Cluster.
It may work for other SLURM systems.

The script parses the STDOUT for the `squeue -u $USER` commands into a Pandas dataframe.
Using Pandas, ths script then filters out all running processes.
The script then finds all `slurm-xxxxx.out` in your home directory, and removes all slurm out files that are not running processes.