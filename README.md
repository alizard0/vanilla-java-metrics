# vanilla-java-metrics
Vanilla java program with metrics powered by micrometer-prometheus. 
No java-framework (spring, springboot, struts or quarkus) was used. 

1. clone the project
2. run `$ mvn clean package`
3. run `$ java -jar target/vanilla-java-metrics-1.0-SNAPSHOT-jar-with-dependencies.jar`
```bash
alizardo@alizardo-mac vanilla-java-metrics % java -jar target/vanilla-java-metrics-1.0-SNAPSHOT-jar-with-dependencies.jar
Server started on http://localhost:8081/metrics

```
4. On your browser, go to http://localhost:8081/metrics
```
# HELP disk_free_bytes Usable space for path
# TYPE disk_free_bytes gauge
disk_free_bytes{path="/"} 1.51144132608E11
# HELP disk_total_bytes Total space for path
# TYPE disk_total_bytes gauge
disk_total_bytes{path="/"} 4.94384795648E11
# HELP jvm_buffer_count_buffers An estimate of the number of buffers in the pool
# TYPE jvm_buffer_count_buffers gauge
jvm_buffer_count_buffers{id="direct"} 1.0
jvm_buffer_count_buffers{id="mapped"} 0.0
# HELP jvm_buffer_memory_used_bytes An estimate of the memory that the Java virtual machine is using for this buffer pool
# TYPE jvm_buffer_memory_used_bytes gauge
jvm_buffer_memory_used_bytes{id="direct"} 8192.0
jvm_buffer_memory_used_bytes{id="mapped"} 0.0
# HELP jvm_buffer_total_capacity_bytes An estimate of the total capacity of the buffers in this pool
# TYPE jvm_buffer_total_capacity_bytes gauge
jvm_buffer_total_capacity_bytes{id="direct"} 8192.0
jvm_buffer_total_capacity_bytes{id="mapped"} 0.0
# HELP jvm_gc_live_data_size_bytes Size of long-lived heap memory pool after reclamation
# TYPE jvm_gc_live_data_size_bytes gauge
jvm_gc_live_data_size_bytes 0.0
# HELP jvm_gc_max_data_size_bytes Max size of long-lived heap memory pool
# TYPE jvm_gc_max_data_size_bytes gauge
jvm_gc_max_data_size_bytes 4.294967296E9
# HELP jvm_gc_memory_allocated_bytes_total Incremented for an increase in the size of the (young) heap memory pool after one GC to before the next
# TYPE jvm_gc_memory_allocated_bytes_total counter
jvm_gc_memory_allocated_bytes_total 0.0
# HELP jvm_gc_memory_promoted_bytes_total Count of positive increases in the size of the old generation memory pool before GC to after GC
# TYPE jvm_gc_memory_promoted_bytes_total counter
jvm_gc_memory_promoted_bytes_total 0.0
# HELP jvm_memory_committed_bytes The amount of memory in bytes that is committed for the Java virtual machine to use
# TYPE jvm_memory_committed_bytes gauge
jvm_memory_committed_bytes{area="heap",id="G1 Eden Space"} 2.7262976E7
jvm_memory_committed_bytes{area="heap",id="G1 Old Gen"} 2.4117248E8
jvm_memory_committed_bytes{area="heap",id="G1 Survivor Space"} 0.0
jvm_memory_committed_bytes{area="nonheap",id="CodeHeap 'non-nmethods'"} 2555904.0
jvm_memory_committed_bytes{area="nonheap",id="CodeHeap 'non-profiled nmethods'"} 2555904.0
jvm_memory_committed_bytes{area="nonheap",id="CodeHeap 'profiled nmethods'"} 2555904.0
jvm_memory_committed_bytes{area="nonheap",id="Compressed Class Space"} 1310720.0
jvm_memory_committed_bytes{area="nonheap",id="Metaspace"} 1.1010048E7
# HELP jvm_memory_max_bytes The maximum amount of memory in bytes that can be used for memory management
# TYPE jvm_memory_max_bytes gauge
jvm_memory_max_bytes{area="heap",id="G1 Eden Space"} -1.0
jvm_memory_max_bytes{area="heap",id="G1 Old Gen"} 4.294967296E9
jvm_memory_max_bytes{area="heap",id="G1 Survivor Space"} -1.0
jvm_memory_max_bytes{area="nonheap",id="CodeHeap 'non-nmethods'"} 5849088.0
jvm_memory_max_bytes{area="nonheap",id="CodeHeap 'non-profiled nmethods'"} 1.22912768E8
jvm_memory_max_bytes{area="nonheap",id="CodeHeap 'profiled nmethods'"} 1.22896384E8
jvm_memory_max_bytes{area="nonheap",id="Compressed Class Space"} 1.073741824E9
jvm_memory_max_bytes{area="nonheap",id="Metaspace"} -1.0
# HELP jvm_memory_used_bytes The amount of used memory
# TYPE jvm_memory_used_bytes gauge
jvm_memory_used_bytes{area="heap",id="G1 Eden Space"} 9437184.0
jvm_memory_used_bytes{area="heap",id="G1 Old Gen"} 0.0
jvm_memory_used_bytes{area="heap",id="G1 Survivor Space"} 0.0
jvm_memory_used_bytes{area="nonheap",id="CodeHeap 'non-nmethods'"} 1129984.0
jvm_memory_used_bytes{area="nonheap",id="CodeHeap 'non-profiled nmethods'"} 253440.0
jvm_memory_used_bytes{area="nonheap",id="CodeHeap 'profiled nmethods'"} 1396608.0
jvm_memory_used_bytes{area="nonheap",id="Compressed Class Space"} 1109368.0
jvm_memory_used_bytes{area="nonheap",id="Metaspace"} 1.0586832E7
# HELP jvm_threads_daemon_threads The current number of live daemon threads
# TYPE jvm_threads_daemon_threads gauge
jvm_threads_daemon_threads 5.0
# HELP jvm_threads_live_threads The current number of live threads including both daemon and non-daemon threads
# TYPE jvm_threads_live_threads gauge
jvm_threads_live_threads 7.0
# HELP jvm_threads_peak_threads The peak live thread count since the Java virtual machine started or peak was reset
# TYPE jvm_threads_peak_threads gauge
jvm_threads_peak_threads 7.0
# HELP jvm_threads_started_threads_total The total number of application threads started in the JVM
# TYPE jvm_threads_started_threads_total counter
jvm_threads_started_threads_total 8.0
# HELP jvm_threads_states_threads The current number of threads
# TYPE jvm_threads_states_threads gauge
jvm_threads_states_threads{state="blocked"} 0.0
jvm_threads_states_threads{state="new"} 0.0
jvm_threads_states_threads{state="runnable"} 4.0
jvm_threads_states_threads{state="terminated"} 0.0
jvm_threads_states_threads{state="timed-waiting"} 2.0
jvm_threads_states_threads{state="waiting"} 1.0
# HELP process_cpu_time_ns_total The "cpu time" used by the Java Virtual Machine process
# TYPE process_cpu_time_ns_total counter
process_cpu_time_ns_total 3.50661E8
# HELP process_cpu_usage The "recent cpu usage" for the Java Virtual Machine process
# TYPE process_cpu_usage gauge
process_cpu_usage 0.0
# HELP process_start_time_seconds Start time of the process since unix epoch.
# TYPE process_start_time_seconds gauge
process_start_time_seconds 1.734975574884E9
# HELP process_uptime_seconds The uptime of the Java virtual machine
# TYPE process_uptime_seconds gauge
process_uptime_seconds 2.627
# HELP system_cpu_count The number of processors available to the Java virtual machine
# TYPE system_cpu_count gauge
system_cpu_count 10.0
# HELP system_cpu_usage The "recent cpu usage" of the system the application is running in
# TYPE system_cpu_usage gauge
system_cpu_usage 0.0
# HELP system_load_average_1m The sum of the number of runnable entities queued to available processors and the number of runnable entities running on the available processors averaged over a period of time
# TYPE system_load_average_1m gauge
system_load_average_1m 1.57275390625
```
