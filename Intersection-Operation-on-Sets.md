# Intersection-Operation-on-Sets
write a program in c to create two sets and perform the intersection operation on sets.

A Set is a collection of well defined and distinct objects. Intersection of two sets A and B is defined as, all the elements of set A, which are also elements of set B. Union of two sets A and B is defined as, all the elements of A and B, but not belonged to both.

Here your task is to ask user to enter any elements in a set of array and you have to extract the common elements among the set. For example lets us consider an array 
```a[2, 4, 6, 8] ```
and 
``` b[2, 5, 7, 11]```
Then common element is 2

## C Program - Intersection of Array
 ### C program to find intersecting elements from 2 arrays.
````
#include <stdio.h>
int main()
{
int a[10], b[10], flag = 0, n1, n2, i, j;
printf("Enter array1 size : ");
scanf("%d",&n1);
printf("\nEnter array2 size : ");
scanf("%d",&n2);
printf("\nEnter array1 element : ");
for(i = 0;i < n1;i++)
scanf("%d",&a[i]);
printf("\nEnter array2 element : ");
for(i = 0;i < n2;i++)
scanf("%d",&b[i]);
printf("Intersection: ");
for(i = 0;i < n1;i++)
{
for(j = 0;j < n2;j++)
{
if(b[i] == a[j])
{
flag = 1;
}
}
if(flag == 1)
{
printf("%d ", b[i]);
}
flag = 0;
}
return 0;
}

Enter array1 size : 5
Enter array2 size : 3
Enter array1 element : 1 2 3 4 5
Enter array2 element : 1 2 6
Intersection: 1, 2
```
Note:
Here we have two arrays, we compare every individual elements of one array(b[]) to elements in another array(a[]), if any of the element matches we raise the flag = 1 and print that particular element. This process is repeated until it reaches the last element in an array(b[]).
