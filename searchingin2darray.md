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

using namespace std;

int main()
{
   int n,m;
   cin>>n>>m;
   
   int arr[n][m];
   for(int i=0;i<n;i++){
       for(int j=0;j<m;j++){
           cin>>arr[i][j];
       }
   }
   
   
   cout<<"matrix is\n";
   for(int i=0;i<n;i++){
       for(int j=0;j<m;j++){
           cout<<arr[i][j];
       }
       cout<<"\n";
   }
   
   int x;
   cin>>x;
   
   bool flag=false;
   for(int i=0;i<n;i++){
       for(int j=0;j<m;j++){
           if(arr[i][j]==x){
               cout<<i<<" "<<j<<"\n";
               flag = true;
           }
       }
   }
   
   
   if(flag){
       cout<<"elements found\n";
   }
   else{
       cout<<"elements not found\n";
   }
    return 0;
}
