# cprograms
An array is a container object that holds a fixed number of values of a single type. To create an array in C, we can do int arr[n];. Here, arr, is a variable array which holds up to  integers. The above array is a static array that has memory allocated at compile time. A dynamic array can be created in C, using the malloc function and the memory is allocated on the heap at runtime. To create an integer array,  of size , int *arr = (int*)malloc(n * sizeof(int)), where  points to the base address of the array.
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>


int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int *val = malloc(n*sizeof(int));
    for(int i=0;i<n;i++)
    {
        scanf("%d",&val[i]);
        sum+=val[i];
    }
    printf("%i",sum);
    free(val);
}
