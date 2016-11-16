Values inserted in the excel file:

``` 
Worker vcores	20
Worker spindles	12
Worker RAM	128
Workload factor	10
Worker nodes	10
``` 


Regarding memory choosen in the excel file. 
The OS memory could be to high/low if we select always 10% of the total RAM memory. Good practice is to start considering 8-10 Gb of RAM only fo the OS and then tune it.
The other components has a reasonable estimation of memory. Like `max.heap` is about 75% of `mapreduce.[map|redce].memory.mb` as suggested by the guidelines.
