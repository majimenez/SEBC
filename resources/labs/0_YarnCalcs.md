<b>1. Inspect the derived/default values. Adjust as necessary.</b>

Parameters Settings: <br/>
<ul>
<li>Worker vcores	20</li>
<li>Worker spindles	12</li>
<li>Worker RAM	128</li>
<li>Workload factor	2</li>
<li>Worker nodes	10</li>
</ul>

Comments:<br>
<ul>
<li>
memory addressed to OS is too high for a worker node. The best is to give about 0,7% (aprox.9G) of the OS memory is more than enough.
</li>
<li>(Cell F2) yarn.nodemanager.resource.cpu-vcores * "workload factor" to allow to execute more tasks per CPU</li>
</ul>
<b>2. What criteria affects workload factor? What does a value of 1, 2, or 4 signify?</b>


The workload factor is affected by the number of tasks that are being executed by a core:<br/>
<ul>
<li>Workload factor = 1 for the execution of a task per core</li>
<li>Workload factor = 2 for the execution of two tasks per core</li>
<li>Workload factor = 4 for the execution of four tasks per core</li>
</ul>