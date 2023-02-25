# calendar_1st-work
Hello, this is my very first project of making a calendar. nothing creative.


#include<stdio.h>
    int firstday(int year)
    {
        int day = (year*365+((year-1)/4) - ((year-1)/100) + ((year-1)/400))%7 ;
        return day;
    }
int main()
{
    char *month[]= {"JANUARY","FEBRUARY","MARCH","APRIL","MAY","JUNE","JULY","AUGUST","SEPTEMBER","OCTOBER","NOVEMBER","DECEMBER" };
    int days[] = {31,28,30,31,30,31,30,31,30,31,30,31};
    int x,i,y,j,totaldays,weekend=0,spacecounter=0,year;
    printf("enter your favourite year :\n ");
    scanf("%d",&year);
    printf("welcome to %d\n\n",year);

    if(year%4==0 && year%100!=0 || year%400==0)
    {
      days[1] =  29;
    }
    weekend =firstday(year);
    for(i=0;i<12;i++)
    {
        printf("\n\n\n ----------------- %s -----------------\n",month[i]);
        printf("\n       SUN     MON    TUE   WED    FRI  SAT\n\n");
        for(spacecounter=1;spacecounter<=weekend;spacecounter++)
        {
            printf("      ");
        }
        totaldays= days[i];
        for(j=1;j<=totaldays;j++)
        {
            printf("%6d",j);
            weekend++;
            if(weekend>6){
            weekend=0;
            printf("\n");
            }
        }
    }
    return 0;
}







very first project...created 6 month ago.
