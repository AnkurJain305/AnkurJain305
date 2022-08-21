### Hi there 👋

<!--
**AnkurJain305/AnkurJain305** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
#include <iostream>
#include<climits>//dont forget to use this header file
using namespace std;

int kadane(int arr[],int n){
    int currentsum=0;
   int maxsum=INT_MIN;
   for(int i=0;i<n;i++){
       currentsum+=arr[i];
       if(currentsum<0){
           currentsum=0;
       }
       maxsum=max(maxsum,currentsum);
   }
   return maxsum;
}

int main()
{
   int n;
   cin>>n;
   
   int arr[n];
   for(int i=0;i<n;i++){
       cin>>arr[i];
   }
   
   int wrapsum;
   int nonwrapsum;
   
   nonwrapsum=kadane(arr,n);
   int totalsum=0;
   for(int i=0;i<n;i++){
       totalsum+=arr[i];
       arr[i]= -arr[i];
   }
   
   wrapsum=totalsum+kadane(arr,n);
   
   
   cout<<max(wrapsum,nonwrapsum)<<endl;
    return 0;
}
