#include <stdio.h>
int main()
{
int wait[20], bur[20], turn[20];
int num, i, j, t, id[20], temp, burst[20];
float avgwt=0, avgturn=0;
printf("\nImplementation of the SJF algorithm\n"); 
printf("\n Enter the number of process:");  //Declare the How Many Process Want to Use. 
scanf("%d", &num);
for(i=0; i<num; i++)
{
printf("\n Enter the burst time for process p%d:", i+1);  //Declare the BurstTime in Each Process.
scanf("%d", &bur[i]);
burst[i]=bur[i];
id[i]=i+1;
}
for(i=0; i<num; i++)    //Condition of SJF..
{
for(j=i+1; j<num; j++)
{
if(bur[i]>=bur[j])
{
t=bur[i];
bur[i]=bur[j];
bur[j]=t;
temp=id[i];
id[i]=id[j];
id[j]=temp;
}
}
}
wait[id[0]-1]=0;
temp=0;
for(i=1; i<=num; i++)
{
wait[id[i]-1]=bur[i-1]+temp;  //Calculation of WaitingTime.
temp=wait[id[i]-1];
}
printf("\nGANTT CHART");   //Create Gantt Chart.
printf("\n________________________________________________________\n");
for(i=0; i<num; i++)
printf("    p%d  |",id[i]);
printf("\n________________________________________________________\n");
for(i=0; i<=num; i++)
printf("%d\t",wait[id[i]-1]);        //Allocate the WaitingTime in Each Process..
printf("\n\n\n_____________________________________________________________\n");   // Create Calculation Table.
printf("\n PROCESS    BURSTTIME     WAITINGTIME      TURNAROUNDTIME\n");
printf("\n________________________________________________________________\n");
for(i=0; i<num; i++)
{
turn[i]=wait[i]+burst[i];        //Calculate the TurnAroundTime..
printf("\np%d\t\t%d\t\t%d\t\t%d", i+1, burst[i], wait[i], turn[i]);
avgwt=avgwt+wait[i];        //Calculate the Average WaitingTime.
avgturn=avgturn+turn[i];    //Calculate the Average  TurnAroundTime.
}
printf("\n\nAverage waiting time is %f ms", avgwt/num);
printf("\nAverage Trun around time is %f ms", avgturn/num);
}
