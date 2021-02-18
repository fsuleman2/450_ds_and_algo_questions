# 450_ds-algo_question
### 1. Write a C++ program to reverse an array
```c++
#include<iostream>
#include<stdio.h>
#include<bits/stdc++.h>
using namespace std;
int reverse_array(int a[],int n)
{
    int temp;
    int start = 0 ;
    int end = n-1;
    while(start < end)
    {
        temp = a[start];
        a[start] = a[end];
        a[end] = temp;
        start ++;
        end --;
    }
    
}
//Function for printing an array
void printArray(int a[],int size)
{
     for(int i = 0 ; i < size; i++)
    {
        cout<<a[i]<<" ";
        cout<<endl;
    }
}
int main()
{
    cout<<"REVERSING AN ARRAY"<<endl;
    int n;
    cout<<"Enter the number of elements you want to revers"<<endl;
    cin>>n;
    //declaring an array
    int a[n];
    //accepting elements into the array
    cout<<"Enter the elements"<<endl;
    for(int i = 0 ; i < n; i++)
    {
        cin>>a[i];
    }
    reverse_array(a,n);
    cout<<"Reverse Elements are"<<endl;
    printArray(a,n);
    return 0;

}
```
