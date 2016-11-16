Values inserted in the excel file:

``` 
Worker vcores	20
Worker spindles	12
Worker RAM	128
Workload factor	2
Worker nodes	10
``` 


Regarding memory choosen in the excel file. 
The OS memory could be to high/low if we select always 10% of the total RAM memory (if we have 32 GB of RAM, The Os memory would be too low, if we have 256 GB of ram it will be to high). Good practice is to start considering 8-10 Gb of RAM only for the OS and then tune it.
The other components has a reasonable estimation of memory. Like `max.heap` is about 75% of `mapreduce.[map|redce].memory.mb` as suggested by the guidelines.


The workload factor is used to configure the maximum number of mappers and reducer on the gateway rule. It impacts the number of mappers and reducers that we expect to run on each worker node. This is limited only if the resources are not enough to cope with the expected workload, the maximum amount of mappers/reducers is limited by the more "scarse" resource (memory or the vcores).
