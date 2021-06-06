Total nymber of ways to reach nth stair 
https://www.geeksforgeeks.org/count-ways-reach-nth-stair/
#include<bits/stdc++.h>
using namespace std;
int dyp(int n, vector<int>&dp){
    int ans1 =0,ans2=0;
    if(n<=1){
     return n;
    }
    if(dp[n]!=-1){
    return dp[n];
    }
     
   ans1 =  dyp(n-1,dp);
 
   ans2 = dyp(n-2,dp);
return dp[n] = ans1 + ans2;
}
int main(){
int n;
cin>>n;
vector<int> dp(n+2,-1);
cout<<dyp(n+1,dp);
    return 0;
}

