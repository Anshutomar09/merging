# merging

//merging of two array 
#include <iostream>
#include<vector> 

using namespace std;
void merge(int arr1[],int n,int arr2[],int m,int arr3[]){
    int i=0,j=0,k=0;
    while(i<n&&j<m){
        if(arr1[i]<=arr2[j]){
            arr3[k++]=arr1[i++];
        }
        else{
            arr3[k++]=arr2[j++];
        }
    }
    while(n>i){
        arr3[k++]=arr1[i++];
    }
    while(m>j){
        arr3[k++]=arr2[j++];
    }
}
void print(int arr3[], int n )
{
    for(int i=0;i<n;i++){
        cout<<arr3[i]<<" ";
    }
    cout<<endl;
}

int main()
{
   
   int arr1[5]={1,3,5,8,10};
   int arr2[6]={2,4,6,7,9,11};
   int arr3[11]={0};
   merge(arr1,5,arr2,6,arr3);
   print(arr3,11);
    
}
