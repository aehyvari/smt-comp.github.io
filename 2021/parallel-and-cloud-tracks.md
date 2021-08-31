---
figures:
- par-cloud-analysis/2019-Par4_vs_Par4_cloud.png
- par-cloud-analysis/2019-Par4_vs_Par4_parallel.png
- par-cloud-analysis/OpenSMT_vs_SMTS cube-and-conquer_cloud.png
- par-cloud-analysis/OpenSMT_vs_SMTS portfolio_cloud.png
- par-cloud-analysis/SMTS portfolio_vs_SMTS cube-and-conquer_cloud.png
- par-cloud-analysis/STP_vs_STP-CMS-Cloud_cloud.png
- par-cloud-analysis/STP_vs_STP-parallel_parallel.png
- par-cloud-analysis/Vampire_vs_Vampire-Parallel_cloud.png
- par-cloud-analysis/Vampire_vs_Vampire-Parallel_parallel.png
- par-cloud-analysis/cloud_Arith.png
- par-cloud-analysis/cloud_Bitvec.png
- par-cloud-analysis/cloud_Equality+LinearArith.png
- par-cloud-analysis/cloud_Equality+MachineArith.png
- par-cloud-analysis/cloud_Equality+NonLinearArith.png
- par-cloud-analysis/cloud_Equality.png
- par-cloud-analysis/cloud_QF_Bitvec.png
- par-cloud-analysis/cloud_QF_Equality+Bitvec.png
- par-cloud-analysis/cloud_QF_Equality+NonLinearArith.png
- par-cloud-analysis/cloud_QF_FPArith.png
- par-cloud-analysis/cloud_QF_LinearIntArith.png
- par-cloud-analysis/cloud_QF_LinearRealArith.png
- par-cloud-analysis/cloud_QF_NonLinearIntArith.png
- par-cloud-analysis/cloud_QF_NonLinearRealArith.png
- par-cloud-analysis/cvc5_vs_cvc5-gg_cloud.png
- par-cloud-analysis/cvc5_vs_cvc5-gg_parallel.png
- par-cloud-analysis/parallel_Arith.png
- par-cloud-analysis/parallel_Bitvec.png
- par-cloud-analysis/parallel_Equality+LinearArith.png
- par-cloud-analysis/parallel_Equality+MachineArith.png
- par-cloud-analysis/parallel_Equality+NonLinearArith.png
- par-cloud-analysis/parallel_Equality.png
- par-cloud-analysis/parallel_QF_Bitvec.png
- par-cloud-analysis/parallel_QF_Equality+Bitvec.png
- par-cloud-analysis/parallel_QF_Equality+NonLinearArith.png
- par-cloud-analysis/parallel_QF_FPArith.png
- par-cloud-analysis/parallel_QF_LinearIntArith.png
- par-cloud-analysis/parallel_QF_LinearRealArith.png
- par-cloud-analysis/parallel_QF_NonLinearIntArith.png
- par-cloud-analysis/parallel_QF_NonLinearRealArith.png
---

## Parallel and Cloud Tracks

This year we are organising new, experimental, cloud and parallel tracks
for SMT-COMP.  Similar tracks were organised in the SAT competition 2020
and the competition had a positive impact on the development of parallel
SAT solvers (see <https://satcompetition.github.io/2020/>).

### The Concept

The goal in both the cloud and the parallel tracks is to measure the
success of a solver in solving a single, hard instance.  This will be done by
giving solvers instances one at a time, similar to the SMT-COMP single-query
track.  The participating solvers will be scored based on the number of
instances that a solver solves within the per-instance wall-clock time limit
and the total run time, similar to the single-query track’s parallel score.

For these tracks we chose in total slightly over 400 benchmarks from the
single-query track logics.  All instances should come from the smt-lib
benchmark library.

The solver submission rules follow those of the rest of the tracks.  However,
on this track we do accept portfolio solvers, as defined in the rules, as
competitors.  We encourage submission of non-portfolio solvers and reserve the
right to give special mentions to non-portfolio solvers in reporting the
results.

While the standard competition will be run in StarExec, the parallel and cloud
tracks will be run on Amazon Web Services.  AWS has kindly agreed to sponsor
the participants in the testing phase.

The information for participation is stored
[here](parallel-and-cloud-tracks-participation.html) for documentation purposes.

### Analysis of the results
{% for pic in page.figures %}
  <img src="{{pic}}"/>
{% endfor %}
