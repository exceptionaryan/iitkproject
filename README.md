# iitkproject
#include <stdio.h>
#include <time.h>
clock_t t;//initialiose clock
long int i=0;// number of times code run
void speed_check()
{
    printf("program starts \n");
    while(1)
    {// loop 
    if(t==1000000) break;// break for 1 sec 
    i=i+1;// update number of time 
    t = clock() - t;// time update 
    }
}
int main()
{
    t = clock();// clock 
    speed_check();// call function
    double time_taken = ((double)t)/CLOCKS_PER_SEC; // in seconds
    printf("program excecutes %ld time in %f seconds \n",i,time_taken);
    printf("program ends \n");
    return 0;
}
