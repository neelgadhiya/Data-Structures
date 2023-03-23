//merge sort 
#include<stdio.h> 
#include<stdlib.h> 
  void printarray(int *A,int sz) 
  { 
    for(int i=0;i<sz;i++) 
    { 
      printf("%d ",A[i]); 
    } 
  } 
 void merge(int *A,int low,int mid,int high) 
{ 
  int i,j,k,B[high+1]; 
  i=low; 
  j=mid+1; 
  k=low; 
  while(i<=mid && j<=high) 
  { 
    if(A[i]<A[j]) 
    { 
      B[k]=A[i]; 
      i++; 
      k++; 
    } 
    else 
    { 
      B[k]=A[j]; 
      j++; 
      k++; 
    } 
} 
while(i<=mid) 
{ 
  B[k]=A[i]; 
  i++; 
  k++;
} 
while(j<=high) 
{ 
  B[k]=A[j]; 
  j++; 
  k++; 
} 
for(i=low;i<=high;i++) 
{ 
  A[i]=B[i]; 
} 
} 
void merge_sort(int *A,int low,int high) 
{ 
  int mid; 
  if(low<high) 
  { 
    mid=(low+high)/2; 
    merge_sort(A,low,mid); 
    merge_sort(A,mid+1,high); 
    merge(A,low,mid,high); 
   } 
} 
int main() 
{ 
  int* a; 
  int n,i; 
  printf("\nenter the size of array:"); 
  scanf("%d",&n); 
  printf("\nenter the elements:\n"); 
  a=(int *)malloc(n*sizeof(int)); 
  for(i=0;i<n;i++) 
  { 
    scanf("%d",&a[i]); 
  } 
  printf("\nyour elements before sorting:"); printarray(a,n); 
  printf("\nyour elements after sorting:"); 
  merge_sort(a,0,n-1); 
  printarray(a, n); 
}


