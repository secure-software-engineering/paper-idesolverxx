---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Visualizations
---


To evaluate, which jump-functions representation performs best when analyzing LLVM IR generated from real-world C and C++ programs, we visualize our experimental results in several ways.

We use scatter plots showing the IDESolver++ with the proposed jump-functions representations compared to the IDESolver++ using the nested representation inherited from PhASAR's current IDESolver.
The left plot shows the runtime speedup (higher is better), whereas the right plot shows the relative memory usage (smaller is better).

The IDESolver++ was configured to use <span
class="math inline"><em>J</em><em>F</em><sub><em>N</em><em>D</em></sub></span> (blue), <span
class="math inline"><em>J</em><em>F</em><sub><em>N</em></sub></span> (orange), and <span
class="math inline"><em>J</em><em>F</em><sub><em>N</em><em>E</em></sub></span> (green).
The both horizontal lines are set at *1* meaning no speedup.
We use a log-scale to account for the non-linear distribution of speedups.

The target programs are ordered.
In the following, we show the same plots with different orderings for the target programs to reveal any correlations.

## Program Size Ordering

The target programs are sorted in ascending order by their number of LLVM IR instructions.
This is the plot that we show in the paper.

<div class="box">
  <div class="column">
    <!-- ![phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size](img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size.svg) -->
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-size.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-size" width="49%" height=auto />
  </div>
  <div class="column">
    <!-- ![phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size](img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size.svg) -->
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-size" width="49%" height=auto />
  </div>
</div>

## Number of Procedures

The target programs are sorted in ascending order by their number of LLVM IR functions.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-fun.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-fun" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-fun.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-fun" width="49%" height=auto />
  </div>
</div>

## Number of Address-Taken Procedures

The target programs are sorted in ascending order by their number of LLVM IR functions that are address-taken.
Hence, they are candidate targets for indirect calls through a function-pointer.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-addr-fun.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-addr-fun" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-addr-fun.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-addr-fun" width="49%" height=auto />
  </div>
</div>

## Number of Globals

The target programs are sorted in ascending order by their number of global variables + global constants in LLVM IR.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-global.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-global" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-global.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-global" width="49%" height=auto />
  </div>
</div>

## Number of Call-Sites

The target programs are sorted in ascending order by their number of LLVM IR call-sites.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-calls.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-calls" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-calls.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-calls" width="49%" height=auto />
  </div>
</div>

## Number of Indirect Call-Sites

The target programs are sorted in ascending order by their number of indirect LLVM IR call-sites, i.e., through a function-pointer.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-ind-calls.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-ind-calls" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-ind-calls.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-ind-calls" width="49%" height=auto />
  </div>
</div>

## Number of Basic Blocks

The target programs are sorted in ascending order by their number basic blocks in LLVM IR.

<div class="box">
  <div class="column">
    <img src="img/phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-ind-blocks.svg" alt="phasar-iter-ide-speedup-target-scatter-vs-nested-sorted-ind-blocks" width="49%" height=auto />
  </div>
  <div class="column">
    <img src="img/phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-blocks.svg" alt="phasar-iter-ide-mem-speedup-target-scatter-vs-nested-sorted-blocks" width="49%" height=auto />
  </div>
</div>

<style media="screen">
.box {
  display: flex;
  flex-wrap: wrap;
  padding: 0 4px;
}

.column {
  border-bottom:1px solid gray;
  flex: 50%;
  max-width: 50%;
  min-width: 50%;
  padding: 4px 4px;
  margin-bottom: 1ex;
  text-align: center;
}

.column img {
  margin-bottom: 8px;
  vertical-align: middle;
  width: 100%;
}
</style>