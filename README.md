# 450_ds-algo_question :rocket:
### 1(a). Write a C++ program to reverse an array
```c++
#include<iostream>
#include<stdio.h>
#include<bits/stdc++.h>
using namespace std;

//Function for reversing
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
<hr>

### 1(b). Write a C++ program to reverse a string
```c++
#include<iostream>
#include<stdio.h>
#include<bits/stdc++.h>
using namespace std;

int main()
{
    string str;
    cin>>str;
    reverse(str.begin(),str.end());
    cout<<str;
    /*Manual way to do it
    int len = size(str);
    for(int i=len;i>=0;i--)
    {
        cout<<str[i];
    }
    */
    return 0;
}
```
<hr>

### 2(a). Write a C++ program to find min and max element in an array
```c++
#include<iostream>
#include<bits/stdc++.h>
using namespace std;
int main()
{
  int arr[] = {1000, 11, 445,199,330,300};
  int len = size(arr);
  int max=0;
  for(int i=0; i<len ; i++)
  {
    if(arr[i]>max)
    {
      max=arr[i];
    }
  }
  int min=max;
  for(int i=0;i<len;i++)
  {
    if(arr[i]<min)
    {
      min= arr[i];
    }
  }
  cout<<"Maximum Element "<<max<<endl;
  cout<<"Minimum Element "<<min;
}
```
<hr>

### 2(b). Write a C++ program to find middle of Three
```c++
#include<iostream.h>
#include<stdio.h>
int main()
{
    int A,B,C;
    cin>>A;
    cin>>B;
    cin>>C;
    if((A<B && A>C) || (A>B && A<C) ){
        return A;
    }
    else if((B>A && B<C) || (B<A && B>C)){
        return B;
    }
    else{
        return C;
    }
}
```
<hr>

### 3. Write a program to find kth min element in the array
```python
def kthSmallest_element(arr,k):
    arr.sort()
    return arr[k-1]
#Driver code
#number of elements in the array/list
n= int(input())
arr = []
for i in range(n):
    ins =int(input())
    arr.append(ins)
k = int(input("enter key"))
print(kthSmallest_element(arr,k))

# Input:
> n = 6
> arr[] = 7 10 4 3 20 15
> k = 3
# Output: 7
```
