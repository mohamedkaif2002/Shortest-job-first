Shortest-job-first(SJF)

ALGORITHM:
1.	Read the number of processes and burst time of each processes.
2.	Sort all the processes based on their burst time in the ASCENDING ORDER.
3.	The waiting time of the 1st process in the sequence is zero.
4.	For the other processes, the waiting time of the process is computed as the sum of the waiting time of previous process and the burst time of the previous process.
5.	Draw the Gantt chart and the display the sequence in which the process is served in the Gantt chart.
6.	Compute the turnaround time of all processes as the sum of the waiting time of the process and the burst time of the processes.
7.	Compute the average turnaround time and the average waiting time.

OUTPUT LIKE THIS:

 Enter the number of process:3

 Enter the burst time for process p1:25

 Enter the burst time for process p2:40

 Enter the burst time for process p3:30

GANTT CHART
________________________________________________________
     |   P1   |   P3   |   P2   |
________________________________________________________
     0        25       55       95

________________________________________________________________
 PROCESS      BURSTTIME      WAITINGTIME       TURNAROUNDTIME
________________________________________________________________
P1               25               0                   25
P2               40               55                  95
P3               30               25                  55


Average waiting time is 26.666ms
Average Trunaround time is 58.333ms

