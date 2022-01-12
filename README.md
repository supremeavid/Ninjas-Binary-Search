# Ninjas-Binary-Search
#include <iostream>

using namespace std;
int Binary_Search(int arr[], int n, int key){
    int start=0;
    int endd=n-1;
    while(start<=endd){
            int mid= (start + endd)/2;
            if(arr[mid]==key){
                return mid;
            }
            else if(arr[mid]>key){
                endd=mid-1;
            }
            else{
                start=mid+1;
            }

    }
    return -1;
}
void Input_Array(int arr[],int n){
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
}
void Print_Array(int arr[],int n){
    for(int i=0;i<n;i++){
        cout<<arr[i]<<" ";
    }
}


int main()
{
    //This won't work with random arrays, the input array has to be sorted
    int arrat[10000];
    int n;
    cin>>n;

    Input_Array(arrat,n);
    Print_Array(arrat,n);
    int sol=Binary_Search(arrat,n,15);
    cout<<"The given key is at "<<sol<<"th index of Array."<<endl;



    return 0;
}
