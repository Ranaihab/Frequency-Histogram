# Frequency-Histogram
A program that decides which point belong to each bar. Implemented using mpi and openMp
The tasks are distributed as the following:<br/>
&emsp; &emsp;1- Process 0:<br/>
&emsp; &emsp; &emsp;- Take number of bars, points, threads, processes as input<br/>
&emsp; &emsp; &emsp;- Read the datapoints from the file dataset.txt<br/>
&emsp; &emsp; &emsp;- Find the max and min values in the data points to compute the range of each bar.<br/>
&emsp; &emsp; &emsp;- Distribute the data points among the processes.<br/>
<br/>
 &emsp; &emsp;2- All The processes:<br/>
&emsp; &emsp; &emsp;- Fork threads.<br/>
&emsp; &emsp; &emsp;- Distribute data among the threads.<br/>
&emsp; &emsp; &emsp;- Each thread will assign each of its data to the right bar.
