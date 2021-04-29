#include <stdlib.h>
#include <stdio.h>
#include <math.h>
#include <string.h>
#define SEED 35791246

main(int argc, char** argv)
{
    int N=0;
    double x,y;
    int i,count=0;
    double z;
    double pi;

    printf("Enter the number of iterations used to estimate pi: ");
    scanf("%d",&N);

    srand(SEED);
    count=0;
    for ( i=0; i<N; i++) {
        x = (double)rand()/RAND_MAX;
        y = (double)rand()/RAND_MAX;
        z = x*x+y*y;
        if (z<=1) count++;
    }
    //pi=(double)count/N*4;
    //printf("# of trials= %d , estimate of pi is %g \n",N,pi);
    pi=((double)count/(double)N) * 4.0;
    printf("OpenMP : # of trials = %14ld , estimate of pi is %g\n",N,fabs(pi-M_PI));
}
