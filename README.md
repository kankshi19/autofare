# autofare
Calculates the autofare for both day and night time
//Auto fare
#include<stdio.h>
void main()
{
    float km,t,fare;
    int time;
    printf("Enter 1 for Day\nEnter 2 for Night :");
    scanf("%d", &time);
    printf("Enter the distance covered : ");
    scanf("%f", &km);
    printf("Enter the waiting time : ");
    scanf("%f", &t);
    if(time==1 )
    {
        if (km>0 && km<=1.5)
        {
           fare = 23+t*1;
        }
        else
        {
           km = km-1.5;
           fare = 23+km*10+t*1;
        }
    }
    else if (time == 2)
    {
        if (km>0 && km<=1.5)
        {
           fare = 29+t*2;
        }
        else
       {
           km = km-1.5;
           fare = 29+km*20+t*2;
       }
    }
    else
    {
        printf("Invalid Input");
    }

printf("Auto fare is Rs.%f",fare);

}
