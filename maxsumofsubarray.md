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

int main()
{
   int n;
   cin>>n;
   
   int arr[n];
   for(int i=0;i<n;i++){
       cin>>arr[i];
   }
   int maxsum=INT_MIN;
   for(int i=0;i<n;i++){
       for(int j=i;j<n;j++){
           int sum=0;
           for(int k=i;k<=j;k++){
               sum+=arr[k];
              // cout<<arr[k]<<" ";
           }//cout<<endl;
           maxsum = max(maxsum,sum);
       }
   }

cout<<maxsum<<endl;
    return 0;
}
