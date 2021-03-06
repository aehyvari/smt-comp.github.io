---
layout: tools
year: 2019

tools:

- name: Pre-Processor (Benchmark Scrambler)
  repo: https://github.com/SMT-COMP/scrambler
  sources: https://github.com/SMT-COMP/scrambler/archive/smtcomp2019.tar.gz
  tracks:
    - name: track_single_query
      starexec: SMT-COMP 2019 Non-Incremental Scrambler
      starexecid: 551
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-non-incremental-scrambler.tar.xz
    - name: track_incremental
      starexec: SMT-COMP 2019 Incremental Scrambler
      starexecid: 595
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-incremental-scrambler.tar.xz
    - name: track_single_query_challenge
      starexec: SMT-COMP 2019 Non-Incremental Scrambler
      starexecid: 551
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-non-incremental-scrambler.tar.xz
    - name: track_incremental_challenge
      starexec: SMT-COMP 2019 Incremental Scrambler
      starexecid: 595
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-incremental-scrambler.tar.xz
    - name: track_unsat_core
      starexec: SMT-COMP 2019 Unsat-Core Scrambler
      starexecid: 589
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-unsat-core-scrambler.tar.xz
    - name: track_model_validation
      starexec: SMT-COMP 2019 Model-Validation Scrambler
      starexecid: 554
      release: https://github.com/SMT-COMP/scrambler/releases/download/smtcomp2019/SMT-COMP-2019-model-validation-scrambler.tar.xz

- name: Post-Processor
  repo: https://github.com/SMT-COMP/postprocessors
  sources: https://github.com/SMT-COMP/postprocessors/archive/smtcomp2019.tar.gz
  tracks:
    - name: track_single_query
      starexec: SMT-COMP 2019 Non-Incremental
      starexecid: 555
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-non-incremental-post-processor.tar.xz
    - name: track_incremental
      starexec: SMT-COMP 2019 Incremental
      starexecid: 556
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-incremental-post-processor.tar.xz
    - name: track_single_query_challenge
      starexec: SMT-COMP 2019 Non-Incremental
      starexecid: 555
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-non-incremental-post-processor.tar.xz
    - name: track_incremental_challenge
      starexec: SMT-COMP 2019 Incremental
      starexecid: 556
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-incremental-post-processor.tar.xz
    - name: track_unsat_core
      starexec: SMT-COMP 2019 Unsat-Core
      starexecid: 594
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-unsat-core-post-processor.tar.xz
    - name: track_model_validation
      starexec: SMT-COMP 2019 Model-Validation
      starexecid: 587
      release: https://github.com/SMT-COMP/postprocessors/releases/download/smtcomp2019/SMT-COMP-2019-model-validation-post-processor.tar.xz

- name: Trace executor
  repo: https://github.com/SMT-COMP/trace-executor
  sources: https://github.com/SMT-COMP/trace-executor/archive/smtcomp2019.tar.gz
  release: https://github.com/SMT-COMP/trace-executor/releases/download/smtcomp2019/SMT-COMP-2019-trace-executor.tar.xz
  wrapped: https://www.starexec.org/starexec/secure/explore/spaces.jsp?id=369598

---
