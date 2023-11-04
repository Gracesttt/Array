# Array
#include <stdio.h>
#define STD 10

 int main()
{
   int x[10];
   int i;
  
  for(i=0;i<STD;i++){
   printf("Input number in [%d]",i+1);
   scanf("%d",&x[i]);
   }
 
 
 //find min,max
    int max=x[0];
    int min=x[0]; 
  
  for(i=0;i<STD;i++){
        if(max<x[i]) max=x[i];
        if(min>x[i]) min=x[i];
  }
  printf("maximum is %d \n",max);
  printf("minimum is %d \n",min);
  
  
//find which student get min,max 
printf("student ");
  for(i=0;i<STD;i++){
        if(x[i]==max) printf("[%d] ",i+1);
  }
printf("got maximum score\n");

printf("student ");
  for(i=0;i<STD;i++){
        if(x[i]==min) printf("[%d] ",i+1);
  }
printf("got minimum score\n");


//find avg from x[0]-x[9]
float sum=0.0;
float avg;

for(i=0;i<STD;i++){
    sum+=x[i];
}

avg=sum/STD;
printf("average is %.2f\n",avg);


//find which students get A,C,F
for(i=0;i<STD;i++){
    if(x[i]>(avg+0.2*avg)) printf("student[%d] gets A\n",i+1);
    else if(x[i]<(avg-0.2*avg)) printf("student[%d] gets F\n",i+1);
    else printf("student[%d] gets C\n",i+1);
}

    return 0;
}
