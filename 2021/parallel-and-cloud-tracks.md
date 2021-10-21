---
layout: default
plot_path: /2021/plot_data
plot_summary: plot_summary.html
---

## Parallel and Cloud Tracks

In 2021 the SMT-COMP included two new tracks for parallel solvers.  The
goal of these tracks is to showcase how such solvers fare against the
sequential solvers.

In total there were six parallel or cloud solvers that competed in the
new tracks, whereas the main competiton had 20 participants in the
single-query track.

A detailed analysis shows that the parallel solvers are often superior
to the solvers competing in the single-query track.  However, this is
not universally true, and depends on the division.

In this text I try to give my personal interpretation of the situation
from Summer 2021.  **For the pictures only, see <a href="{{
page.plot_summary }}">here</a>**

Antti (antti.hyvarinen@gmail.com)

### The Concept

The parallel solvers competed in two tracks: the *cloud* and the
*parallel* tracks.  In both tracks the idea is to measure how fast a
solver solves single, hard instances.  We chose in total slightly over
400 benchmarks from the single-query track logics as the benchmarks.

The parallel and cloud tracks were run on Amazon Web Services
infrastructure.  The standard competition was run in StarExec.

### <a name="overview"></a> Overview of the Results

The solvers that competed in the parallel and cloud tracks can be
clearly faster than any of the solvers competing in the single-query
track.  However, they can also be slower or indeed "less reliable",
i.e., unsound.

As an example, the parallel version of
[Vampire](participants/vampire-parallel.html) wins the other solvers
with a convenient margin in the [cloud track's Equality
division](results/equality-cloud.html).

<img src="{{ page.plot_path }}/cloud_Equality.svg"/>

It is hard to give a single picture on the performance of solvers that
competed in the 2021 SMT competition parallel and cloud tracks. The SMT
competition, even when considering only the solvers designed to run in
the AWS infrastructure, consists of 18 tracks.  These tracks are
practically independent competitions because in general solvers support,
or are specialised on solving, a subset of these tracks.

For instance, the SMT-COMP [rules](rules.pdf) define track-wide
recognitions.  The following table gives the biggest lead ranking of the
cloud track competitors.

{% assign cloudBiggestLead = site.results_2021 |where: "track", "track_cloud" |where: "recognition", "biggest_lead" | first %}
{% assign participants = site[cloudBiggestLead.participants] %}
{% assign divisions = site.results_2021 |group_by: "track" |where: "name", "track_cloud" |first %}

<table id = "cloud-biggest-lead" class="result sorted">
<thead>
<tr>
<th>Solver</th>
<th>Correct Score</th>
<th>Time Score</th>
<th>Division</th>
<th>Plot</th>
</tr>
</thead>
{% for score in cloudBiggestLead.parallel %}
<tr>
<td>
    {% assign participant = participants | where: "name", score.name |first %}
<a href="{{ participant.url }}">{{ score.name }}</a>
</td>
<td>{{ score.correctScore }}</td>
<td>{{ score.timeScore }}</td>
<td>
    {% assign div = divisions.items |where: "division", score.division |first %}
<a href="{{ div.url }}">{{ score.division }}</a>
</td>
<td>
    {% assign plot = site.plots_2021 |where: "track", "cloud" |where: "division", score.division |first %}
<a href="{{  plot.url }}">{{ plot.name }}</a>
</td>
</tr>
{% endfor %}
</table>

Clicking through the results we can see for instance that in the seven
winning scores only four of the cases the awarded solver actually wins
all the competitors.

<p>

The rules also provide a score for the <em>largest contribution</em>
score. This year the score seems to offer a slightly more consistent
view.  Unfortunately, due to lack of competition, the score could be
defined only for two divisions (the winners in the table are both
my solvers).

{% assign cloudLargestContribution = site.results_2021 |where: "track", "track_cloud" |where: "recognition", "largest_contribution" | first %}
{% assign participants = site[cloudLargestContribution.participants] %}
{% assign divisions = site.results_2021 |group_by: "track" |where: "name", "track_cloud" |first %}

<table id = "cloud-largest-contribution" class="result sorted">
<thead>
<tr>
<th>Solver</th>
<th>Correct Score</th>
<th>Time Score</th>
<th>Division</th>
<th>Plot</th>
</tr>
</thead>
{% for score in cloudLargestContribution.parallel %}
<tr>
<td>
    {% assign participant = participants | where: "name", score.name |first %}
<a href="{{ participant.url }}">{{ score.name }}</a>
</td>
<td>{{ score.correctScore }}</td>
<td>{{ score.timeScore }}</td>
<td>
    {% assign div = divisions.items |where: "division", score.division |first %}
<a href="{{ div.url }}">{{ score.division }}</a>
</td>
<td>
    {% assign plot = site.plots_2021 |where: "track", "cloud" |where: "division", score.division |first %}
<a href="{{  plot.url }}">{{ plot.name }}</a>
</td>
</tr>
{% endfor %}
</table>

<h3>Instance Selection</h3>

The cloud track requires 300 times more computing power in comparison to
the sequential tracks.  Since the sequential tracks already require
roughly two weeks of computing time in the StarExec cluster it would
have been prohibitively expensive to use the same instance selection in
the parallel and cloud tracks. We therefore devised a new instance
selection scheme for the cloud track.

The selection works in three phases.
<ol>
<li>
   Select interesting instances.  We wanted to have instances that are
   not trivial for the solvers, but still maximise the chance that the
   instances are not unsolvable.  The choice made here was to pick two
   categories of instances: those that are hard but likely solvable and
   those that are hard but possibly too hard.  We used the single-query
   track results from the last three years (2018, 2019, 2020) to get an
   idea how difficul the instances are.  Based on these results we chose
   two types of instances: *hard* and *unsolved*.

   An instance is considered *hard* if in the last three years its
   solving was attempted (i.e., it was chosen as a competition
   instance); and there was a year in which it was solved but no solver
   solved it in less than 10 minutes.

   An instance is considered *unsolved* if in the last three years its
   solving was attempted (i.e., it was chosen as a competition instace);
   and there was a year in which no solver solved it.

   Note that these two groups are not mutually disjoint, and it happened
   that four instances in our selection were both hard and unsolved.
   This was in fact unintentional.
</li>
<li>
   Choosing instance numbers.  Our target was to pick 400 instances
   without discriminating any of the logics, and, if possible, choose an
   equal amount of hard and unsolved instances.  The idea is that if two
   logics have sufficiently many instances, the same number of instances
   will be picked from them, and if there are enough both hard and
   unsolved instances, roughly half of the picked instances will be hard
   and the other half unsolved.

   Not all logics have enough hard and unsolved instances.  We
   transferrred this "unused capacity" equally to the other logics which
   still had eligible instances.  Let a logic <em>l</em> have <em>d</em> eligible
   instances but the number of instances to be chosen from <em>l</em> be <em>c >
   d</em>.  Assume further that there are <em>n</em> logics which still have
   eligible at least <em>c</em> instances.  Then the number of instances to
   choose for the remaining logics would be increased by
   <em>ceil((c-d)/n)</em>, where <em>ceil</em> is the ceiling function.

   This leads to an approach where the selection is done iteratively in
   a loop, until at least 400 instances have been chosen.  At each round
   we choose, for each logic, a number of instances that corresponds to
   the minimum available number of instances over all logics.  Once this
   number <em>n</em> is determined, we still need to determine whether there
   are enough hard and unsolved instances for a logic.  If there are, we
   choose <em>ceil(n/2)</em> hard instances and <em>n-ceil(n/2)</em> unsolved
   instances.  If not, we choose all the instances of which there are
   less than <em>ceil(n/2)</em> (say, hard), and the remaining from the other
   instance type (say, unsolved).

   The idea can be visualised as a set of buckets, one per logic, each
   with the volume corresponding to the number of eligible benchmarks
   for that logic.  The task is to fill the buckets with liquid.  We
   start by filling the smallest bucket to the rim and pour the same
   amount of liquid to the rest of the buckets.  Then we remove the full
   buckets and fill the fullest bucket to the rim, pour the same amount
   to the rest of the buckets, and again remove the full buckets.  We
   finish once we have poured at least a 400 l of liquid (corresponding
   to 400 benchmarks), and all the remaining buckets have the same
   amount of liquid.
</li>
<li>
   Once the numbers <em>h_l</em> and <em>u_l</em> of hard and unsolved benchmarks are
   computed for each logic <em>l</em> with the above method, we shuffle the
   benchmarks using the competition seed and python's
   pseudo-random-number-genrator, and pick the first <em>h_l</em> and <em>u_l</em>
   logics.  This is then the final selection.
</li>
</ol>
The code producing the selection is available in <a
href="https://github.com/SMT-COMP/smt-comp/tree/master/2021/prep/selection">the smt-comp github
repository</a>

<p>
We made no effort in choosing satisfiable and unsatisfiable instances in
a balanced way, but instead delegated this to the curators of smt-lib
benchmarks.  It looks like the selection ended up being relatively
balanced.  Based on the SMT-LIB annotations, in the cloud track
selection there are 46 instances marked as `(set-info :status sat)` and
67 instances marked as `(set-info :status unsat)`, while 297 instances
are marked as `(set-info :status unknown)`.

<H3>Lessons Learned</H3>

While it looks like in most cases the instance selection was I am not
happy with how the instances ended up being.  Some benchmarks had no
solvable instances and we had some instances that seem to be too easy.
It could also be that there simply aren't good benchmarks in some of
these cases.

<p>

It might make sense to switch the instance selection from being
logic-based to division-based, since now some divisions that combine
many logics have much more instances.

