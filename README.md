Serial-to-Parallel--Monte-Carlo-Pi
==================================

This tutorial covers how to write a parallel program to calculate π using the Monte Carlo method with MPI and OpenMP. 

####Compiling and Running
Before you start, you will need to edit the submit scripts (submit.pbs and mpisubmit.pbs) and replace AAA123 with the correct project ID. Once done, you need to load the PGI programming environment

```
module load PrgEnv-pgi
```

The code can be simultaneously compiled and submitted via a Make task depending on which version you'd like to run:

* Serial version: `make serial`
* MPI_Reduce verion: `make mpi`
* MPI Send/Recv verion: `make mpisr`
* OpenMP version: `make omp`
* Hybrid OpenMP/MPI version: `make mpiomp`

The output should look something like:

```
Wed Sep 18 11:02:27 EDT 2013
Pi: 3.140800
Application 3587838 resources: utime ~0s, stime ~0s, Rss ~3444, inblocks ~4534, outblocks ~11970
```

The tutorial from which this code is from can be found on the OLCF website at: https://www.olcf.ornl.gov/tutorials/monte-carlo-pi/
