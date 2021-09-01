---
figures:
- 2019-Par4_vs_Par4_cloud:
  average_speedup: 1.6712821642651146
  name: 2019-Par4_vs_Par4_cloud
  total_speedup: 1.403435174281391
  track: cloud
  type: scatter
  x-axis: 2019-Par4
  x-solved: 43
  y-axis: Par4
  y-solved: 65
- 2019-Par4_vs_Par4_parallel:
  average_speedup: 1.7699807531653404
  name: 2019-Par4_vs_Par4_parallel
  total_speedup: 1.5255679084437714
  track: parallel
  type: scatter
  x-axis: 2019-Par4
  x-solved: 45
  y-axis: Par4
  y-solved: 70
- OpenSMT_vs_SMTS cube-and-conquer_cloud:
  average_speedup: 8.277390410502646
  name: OpenSMT_vs_SMTS cube-and-conquer_cloud
  total_speedup: 3.358477596841714
  track: cloud
  type: scatter
  x-axis: OpenSMT
  x-solved: 16
  y-axis: SMTS cube-and-conquer
  y-solved: 22
- OpenSMT_vs_SMTS portfolio_cloud:
  average_speedup: 8.67231098477484
  name: OpenSMT_vs_SMTS portfolio_cloud
  total_speedup: 5.737150633664364
  track: cloud
  type: scatter
  x-axis: OpenSMT
  x-solved: 16
  y-axis: SMTS portfolio
  y-solved: 21
- SMTS portfolio_vs_SMTS cube-and-conquer_cloud:
  average_speedup: 0.8923629129651112
  name: SMTS portfolio_vs_SMTS cube-and-conquer_cloud
  total_speedup: 0.8017481678227094
  track: cloud
  type: scatter
  x-axis: SMTS portfolio
  x-solved: 21
  y-axis: SMTS cube-and-conquer
  y-solved: 22
- STP_vs_STP-CMS-Cloud_cloud:
  average_speedup: 0.5840682253567487
  name: STP_vs_STP-CMS-Cloud_cloud
  total_speedup: 0.9633675703263781
  track: cloud
  type: scatter
  x-axis: STP
  x-solved: 3
  y-axis: STP-CMS-Cloud
  y-solved: 5
- STP_vs_STP-parallel_parallel:
  average_speedup: 1.5942
  name: STP_vs_STP-parallel_parallel
  total_speedup: 1.5942
  track: parallel
  type: scatter
  x-axis: STP
  x-solved: 3
  y-axis: STP-parallel
  y-solved: 1
- Vampire_vs_Vampire-Parallel_cloud:
  average_speedup: 24.877812168186285
  name: Vampire_vs_Vampire-Parallel_cloud
  total_speedup: 2.919143225789132
  track: cloud
  type: scatter
  x-axis: Vampire
  x-solved: 40
  y-axis: Vampire-Parallel
  y-solved: 65
- Vampire_vs_Vampire-Parallel_parallel:
  average_speedup: 65.98186921913953
  name: Vampire_vs_Vampire-Parallel_parallel
  total_speedup: 2.0907762520664246
  track: parallel
  type: scatter
  x-axis: Vampire
  x-solved: 42
  y-axis: Vampire-Parallel
  y-solved: 57
- cloud_Arith:
  division: Arith
  name: cloud_Arith
  track: cloud
  type: cactus
- cloud_Bitvec:
  division: Bitvec
  name: cloud_Bitvec
  track: cloud
  type: cactus
- cloud_Equality+LinearArith:
  division: Equality+LinearArith
  name: cloud_Equality+LinearArith
  track: cloud
  type: cactus
  unsound:
  - name: cvc5-gg
- cloud_Equality+MachineArith:
  division: Equality+MachineArith
  name: cloud_Equality+MachineArith
  track: cloud
  type: cactus
- cloud_Equality+NonLinearArith:
  division: Equality+NonLinearArith
  name: cloud_Equality+NonLinearArith
  track: cloud
  type: cactus
- cloud_Equality:
  division: Equality
  name: cloud_Equality
  track: cloud
  type: cactus
- cloud_QF_Bitvec:
  division: QF_Bitvec
  name: cloud_QF_Bitvec
  track: cloud
  type: cactus
- cloud_QF_Equality+Bitvec:
  division: QF_Equality+Bitvec
  name: cloud_QF_Equality+Bitvec
  track: cloud
  type: cactus
- cloud_QF_Equality+NonLinearArith:
  division: QF_Equality+NonLinearArith
  name: cloud_QF_Equality+NonLinearArith
  track: cloud
  type: cactus
- cloud_QF_FPArith:
  division: QF_FPArith
  name: cloud_QF_FPArith
  track: cloud
  type: cactus
  unsound:
  - name: Par4
- cloud_QF_LinearIntArith:
  division: QF_LinearIntArith
  name: cloud_QF_LinearIntArith
  track: cloud
  type: cactus
- cloud_QF_LinearRealArith:
  division: QF_LinearRealArith
  name: cloud_QF_LinearRealArith
  track: cloud
  type: cactus
- cloud_QF_NonLinearIntArith:
  division: QF_NonLinearIntArith
  name: cloud_QF_NonLinearIntArith
  track: cloud
  type: cactus
- cloud_QF_NonLinearRealArith:
  division: QF_NonLinearRealArith
  name: cloud_QF_NonLinearRealArith
  track: cloud
  type: cactus
- cvc5_vs_cvc5-gg_cloud:
  average_speedup: 18.391274289651996
  name: cvc5_vs_cvc5-gg_cloud
  total_speedup: 0.9232295614131685
  track: cloud
  type: scatter
  unsound:
  - instance: /UFLRA/misc/set14.smt2
    solver: cvc5-gg
  - instance: /UFLRA/misc/list2.smt2
    solver: cvc5-gg
  x-axis: cvc5
  x-solved: 39
  y-axis: cvc5-gg
  y-solved: 79
- cvc5_vs_cvc5-gg_parallel:
  average_speedup: 1.7666461240117073
  name: cvc5_vs_cvc5-gg_parallel
  total_speedup: 0.9037659921031682
  track: parallel
  type: scatter
  unsound:
  - instance: /UFLRA/misc/set14.smt2
    solver: cvc5-gg
  - instance: /UFLRA/misc/list2.smt2
    solver: cvc5-gg
  x-axis: cvc5
  x-solved: 42
  y-axis: cvc5-gg
  y-solved: 84
- parallel_Arith:
  division: Arith
  name: parallel_Arith
  track: parallel
  type: cactus
- parallel_Bitvec:
  division: Bitvec
  name: parallel_Bitvec
  track: parallel
  type: cactus
- parallel_Equality+LinearArith:
  division: Equality+LinearArith
  name: parallel_Equality+LinearArith
  track: parallel
  type: cactus
  unsound:
  - name: cvc5-gg
- parallel_Equality+MachineArith:
  division: Equality+MachineArith
  name: parallel_Equality+MachineArith
  track: parallel
  type: cactus
- parallel_Equality+NonLinearArith:
  division: Equality+NonLinearArith
  name: parallel_Equality+NonLinearArith
  track: parallel
  type: cactus
- parallel_Equality:
  division: Equality
  name: parallel_Equality
  track: parallel
  type: cactus
- parallel_QF_Bitvec:
  division: QF_Bitvec
  name: parallel_QF_Bitvec
  track: parallel
  type: cactus
- parallel_QF_Equality+Bitvec:
  division: QF_Equality+Bitvec
  name: parallel_QF_Equality+Bitvec
  track: parallel
  type: cactus
- parallel_QF_Equality+NonLinearArith:
  division: QF_Equality+NonLinearArith
  name: parallel_QF_Equality+NonLinearArith
  track: parallel
  type: cactus
- parallel_QF_FPArith:
  division: QF_FPArith
  name: parallel_QF_FPArith
  track: parallel
  type: cactus
  unsound:
  - name: Par4
- parallel_QF_LinearIntArith:
  division: QF_LinearIntArith
  name: parallel_QF_LinearIntArith
  track: parallel
  type: cactus
- parallel_QF_LinearRealArith:
  division: QF_LinearRealArith
  name: parallel_QF_LinearRealArith
  track: parallel
  type: cactus
- parallel_QF_NonLinearIntArith:
  division: QF_NonLinearIntArith
  name: parallel_QF_NonLinearIntArith
  track: parallel
  type: cactus
- parallel_QF_NonLinearRealArith:
  division: QF_NonLinearRealArith
  name: parallel_QF_NonLinearRealArith
  track: parallel
  type: cactus
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
[here](parallel-and-cloud-tracks-participation.html) for documentation
purposes.



### Solver comparisons in cloud track

The cactus plots below show results on the solvers submitted to the
cloud track as well as solvers that ran on single-query
track that I ran on starexec.  The cloud track solvers are plotted with
a thicker line.  An asterisk after a solver name indicates that it was
unsound in the division in the cloud track.

{% assign cactus_cloud = page.figures |where: "type", "cactus" |where: "track", "cloud" %}
{% for pic in cactus_cloud %}
#### Track cloud, Division {{ pic.division }}
  <img src="par-cloud-analysis/{{ pic.name }}.svg"/>
  {% if pic.unsound %}
  - Unsound solvers on this track and division:
    {% for solver in pic.unsound %}
    - {{ solver.name }}
    {% endfor %}
  {% endif %}
{% endfor %}

{% assign cactus_parallel = page.figures |where: "type", "cactus" |where: "track", "parallel" %}
{% for pic in cactus_parallel %}
#### Track parallel, Division {{ pic.division }}
  <img src="par-cloud-analysis/{{ pic.name }}.svg"/>
  {% if pic.unsound %}
  - Unsound solvers on this track and division:
    {% for solver in pic.unsound %}
    - {{ solver.name }}
    {% endfor %}
  {% endif %}
{% endfor %}


#### Version comparisons in the cloud track

A version of these solvers were submitted in both cloud and single-query
tracks, allowing a comparison between the two versions.  In case of
SMTS, two versions were submitted to the cloud track.

{% assign scatter_cloud = page.figures |where: "type", "scatter" |where: "track", "cloud" %}
{% for pic in scatter_cloud %}
  <img src="par-cloud-analysis/{{ pic.name }}.svg"/>
  - {{ pic.x-axis }} solved {{ pic.x-solved }} instances.
  - {{ pic.y-axis }} solved {{ pic.y-solved }} instances.
  - {{ pic.y-axis }} is in total {{ pic.total_speedup | round: 2}} times faster than
    {{ pic.x-axis }}
  - {{ pic.y-axis }} is on average {{ pic.average_speedup | round: 2}} times faster than
    {{ pic.x-axis }}
  {% if pic.unsound %}
  - Unsoundnesses:
    {% for unsoundness in pic.unsound %}
    - {{ unsoundness.solver }} is unsound on `{{ unsoundness.instance }}`
    {% endfor %}
  {% endif %}
{% endfor %}


#### Version comparisons in the parallel track

A version of these solvers were submitted in both parallel and single-query
tracks, allowing a comparison between the two versions.

{% assign scatter_parallel = page.figures |where: "type", "scatter" |where: "track", "parallel" %}
{% for pic in scatter_cloud %}
  <img src="par-cloud-analysis/{{ pic.name }}.svg"/>
  - {{ pic.x-axis }} solved {{ pic.x-solved }} instances.
  - {{ pic.y-axis }} solved {{ pic.y-solved }} instances.
  - {{ pic.y-axis }} is in total {{ pic.total_speedup | round: 2}} times faster than
    {{ pic.x-axis }}
  - {{ pic.y-axis }} is on average {{ pic.average_speedup | round: 2 }} times faster than
    {{ pic.x-axis }}
  {% if pic.unsound %}
  - Unsoundnesses:
    {% for unsoundness in pic.unsound %}
    - {{ unsoundness.solver }} is unsound on `{{ unsoundness.instance }}`
    {% endfor %}
  {% endif %}
{% endfor %}

