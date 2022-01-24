# GROMACS benchmark

To aid with standardisation across UK HPC systems, our GROMACS benchmark is identical to the "large" one used by ARCHER, the UK national HPC service.

Details of how to build and run the benchmark may be found in the ARCHER repository here: https://github.com/hpc-uk/archer-benchmarks/tree/master/apps/GROMACS

For the purposes of scoring in procurements, the important result is the performance in nanoseconds/day.

The most recent version of GROMACS installed on our services is 2020.1, built with Intel compiler, MPI and MKL 2019.

# Results

Results for a run on 4 nodes from an ARC cluster (48 cores/node):

```
gmx_mpi mdrun -s nsteps800.tpr -deffnm nc2-cubic-md -ntomp 1 -dlb yes -noconfout -npme 72 
```

```
               Core t (s)   Wall t (s)        (%)
       Time:    75349.454      392.447    19199.9
                 (ns/day)    (hour/ns)
Performance:        0.353       68.048

```

Result `0.353 ns/day`

----------------------
