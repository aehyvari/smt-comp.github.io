## Participation in the cloud and parallel tracks

### Cloud track

The Cloud Track evaluates the effectiveness of parallel SMT solvers to run in a
distributed manner.  The solvers participating in this track will be executed
with a wall-clock time limit of 20 minutes running on 100 m4.4xlarge machines
in parallel. Each m4.4xlarge machine has 16 virtual CPUs and 64 GB memory.
Communication between the machines is possible using MPI and SSH.

Participants of this track are required to submit their solver via a GitHub
repository (which can be private). The repository should contain a docker file
that compiles the solver.  As an example, scripts for account configuration and
instructions to run HordeSAT in the default configuration are available at
<https://github.com/aws-samples/aws-batch-comp-infrastructure-sample>.


### Parallel track

The solvers participating in this track will be executed with a wall-clock time
limit of 20 minutes, thus similar to the Single Query Track.  Each solver will
be run on a single AWS machine of the type m4.16xlarge, which has 64 virtual
cores and 256GB of memory. More details about m4.16xlarge nodes can be found
[here](https://aws.amazon.com/about-aws/whats-new/2016/09/introducing-new-m4-instance-size-m4-16xlarge-and-new-region-availability-of-m4-instances/).

Similar to the Cloud Track, participants of this track are required to submit
their solver via a GitHub repository (which can be private). The repository
should contain a docker file that compiles the solver.

### Solver Submission to Parallel and Cloud Tracks

In order to participate in the Cloud or Parallel Track please send an email to
<aws-smt-comp-2021@googlegroups.com> containing the following:
 1. name of the solver and a list of the authors
 2. your AWS account number
 3. the URL of the GitHub repository including the branch
 4. the full, 40-character SHA-1 hash of the commit

