### Hi there š

<!--
**AnkurJain305/AnkurJain305** is a āØ _special_ āØ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- š­ Iām currently working on ...
- š± Iām currently learning ...
- šÆ Iām looking to collaborate on ...
- š¤ Iām looking for help with ...
- š¬ Ask me about ...
- š« How to reach me: ...
- š Pronouns: ...
- ā” Fun fact: ...
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
