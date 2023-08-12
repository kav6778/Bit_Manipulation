// sum of XOR of all pairs of numbers in the array
// sum of XOR of all subset of numbers in the array
// sum of AND of all pairs of numbers in the array
// sum of AND of all subset of numbers in the array.

#include<bits/stdc++.h>
using namespace std;
#define endl "\n"
#define int long long int

int mod =1e9+7;



int sum_xor_pairs(int arr[], int n){
    int sum_xor =0;
    int temp =0;
    // With the help of bit masking finding the subsets
for(int mask =0; mask<(1<<n); mask++){
    if((__builtin_popcount(mask)) == 2){
        for(int pos =0; pos<n; pos++){
        if((mask>>pos)&1)//if pos is present in mask
            temp ^= arr[pos]; 
        }
        sum_xor = (sum_xor + temp) %mod; //sum of xor of all the subsets
    temp = 0;
    }
    
}
    return sum_xor%mod;
}

int sum_xor_subset(int arr[],int n){
    
    int sum_xor =0;
    int temp =0;
    // With the help of bit masking finding the subsets
for(int mask =0; mask<(1<<n); mask++){
    for(int pos =0; pos<n; pos++){
        if((mask>>pos)&1)//if pos is present in mask
            temp ^= arr[pos]; 
    }
    sum_xor = (sum_xor + temp) %mod; //sum of xor of all the subsets
    temp = 0;
}
return sum_xor%mod;

}

int sum_and_pairs(int arr[], int n){
    int sum_and =0;
    int temp = ~0;
    for(int mask =0; mask<(1<<n); mask++){
    if((__builtin_popcount(mask)) == 2){
        for(int pos =0; pos<n; pos++){
        if((mask>>pos)&1)//if pos is present in mask
            temp &= arr[pos]; 
        }
        sum_and = (sum_and + temp) %mod; //sum of xor of all the subsets
    temp = ~0;
    }
    
}
    return sum_and%mod;
    
}


int sum_and_subset(int arr[],int n){
    
    int sum_and =0;
    int temp = ~0;
    // With the help of bit masking finding the subsets
for(int mask =0; mask<(1<<n); mask++){
    for(int pos =0; pos<n; pos++){
        if((mask>>pos)&1)//if pos is present in mask
            temp &= arr[pos]; 
    }
    sum_and = (sum_and+ temp) %mod; //sum of xor of all the subsets
    temp = ~0;
}
return (sum_and+1)%mod;
}


void solve(){
    int n; cin>>n;
    int arr[n];
    for (int i=0; i<n; i++){
    cin>>arr[i];
    }
    cout<<sum_xor_pairs(arr,n)<<" ";
    cout<<sum_xor_subset(arr,n)<<" ";
    cout<<sum_and_pairs(arr,n)<<" ";
    cout<<sum_and_subset(arr,n)<<" ";
    cout<<endl;
}

signed main(){
    ios_base::sync_with_stdio(0);
    cin.tie(0); cout.tie(0);
    int t; cin>>t;
    while(t--){
        solve();
    }
}






