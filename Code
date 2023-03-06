#include<stdio.h>
#include<math.h>
#include<stdlib.h>
int a[20],count;
int main()
{
int n=4,i,j;
void fourqueen(int row,int n);
printf(" Four Queens Problem Using Backtracking -");
fourqueen(1,n);
return 0;
}
//function for printing the solution
void printfourqueensolution(int n)
{
int i,j;
printf("\n\nThe Possible Solution %d of Four Queen Problem:\n\n",++count);
for(i=1;i<=n;++i)
printf("\t%d",i);
for(i=1;i<=n;++i)
{
printf("\n\n%d",i);
for(j=1;j<=n;++j) //for nxn board
{
if(a[i]==j)
printf("\tQ"); //queen at i,j position
else
printf("\t-"); //empty slot
}
}
}
//function to check conflicts If no conflict for desired position returns 1 otherwise returns 0/
int placequeen(int row,int column)
{
int i;
for(i=1;i<=row-1;++i) {
//checking column and diagonal conflicts
if(a[i]==column)
return 0;
else
if(abs(a[i]-column)==abs(i-row))
return 0;
}
return 1; //no conflicts
}
//function to check for proper positioning of queen
void fourqueen(int row,int n)
{
int column;
for(column=1;column<=n;++column)
{
if(placequeen(row,column))
{
a[row]=column; //no conflicts so place queen
if(row==n) //dead end
printfourqueensolution(n); //printing the board configuration
else //try queen with next position
fourqueen(row+1,n);
}
}
}
