---
layout: default
---
## SMT-COMP 2019 Results

<table id="sequential" class="result sorted">
<thead><tr>
  <th>Solver</th>
  <th>Error Score</th>
  <th>Correctly Solved Score</th>
  <th>CPU time Score</th>
  <th>Solved</th>
  <th>Unsolved</th>
</tr></thead>
    {% for solver in site.single-results.QF_AFBCDE %}
    <tr>
        <td>{{ solver.name }}</td>
        <td>{{ solver.errorScore }}</td>
        <td>{{ solver.correctScore }}</td>
        <td>{{ solver.CPUScore }}</td>
        <td>{{ solver.solved }}</td>
        <td>{{ solver.unsolved }}</td>
    </tr>
    {% endfor %}
<!--
<tr>
  <td>CVC4</td>
  <td>0.000</td>
  <td>35397.747</td>
  <td>188.042</td>
<td>39274</td>
<td>828</td>
</tr><tr>
  <td>MathSAT<SUP><a href="#fn">n</a></SUP></td>
  <td>0.000</td>
  <td>31912.757</td>
  <td>286.331</td>
<td>38570</td>
<td>1532</td>
</tr><tr>
  <td>Minkeyrink-MT</td>
  <td>0.000</td>
  <td>34177.756</td>
  <td>228.504</td>
<td>39327</td>
<td>775</td>
</tr><tr>
  <td>Minkeyrink-ST</td>
  <td>0.000</td>
  <td>35892.846</td>
  <td>172.188</td>
<td>39529</td>
<td>573</td>
</tr><tr>
  <td>STP-CMS-mt-2018</td>
  <td>0.000</td>
  <td>33817.158</td>
  <td>258.014</td>
<td>38421</td>
<td>1681</td>
</tr><tr>
  <td>STP-CMS-st-2018</td>
  <td>0.000</td>
  <td>35215.086</td>
  <td>199.040</td>
<td>38796</td>
<td>1306</td>
</tr><tr>
  <td>STP-Riss-st-2018</td>
  <td>0.000</td>
  <td>34032.066</td>
  <td>232.003</td>
<td>38068</td>
<td>2034</td>
</tr><tr>
  <td>Yices 2.6.0</td>
  <td>0.000</td>
  <td>32801.421</td>
  <td>261.922</td>
<td>39045</td>
<td>1057</td>
</tr><tr>
  <td>z3-4.7.1<SUP><a href="#fn">n</a></SUP></td>
  <td>0.000</td>
  <td>33199.774</td>
  <td>244.757</td>
<td>37349</td>
<td>2753</td>
</tr>
    -->
</table>