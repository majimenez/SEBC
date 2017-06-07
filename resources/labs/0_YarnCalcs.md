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

El "workload factor" afecta al número de tareas que serán ejecutadas por core. <br/>
Siendo:
<ul>
<li>workload factor = 1 para la ejecución de una tarea por core.</li>
<li>workload factor = 2 para la ejecución de 2 tareas por core.</li>
<li>workload factor = 4 para la ejecución de 4 tareas por core.</li>
</ul>