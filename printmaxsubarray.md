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

using namespace std;

int main()
{
   int n;
   cin>>n;
   
   int arr[n];
   for(int i=0;i<n;i++){
       cin>>arr[i];
   }
   
   for(int i=0;i<n;i++){
       for(int j=i;j<n;j++){
           for(int k=i;k<=j;k++){
               cout<<arr[k]<<" ";
           }cout<<endl;
       }
   }

    return 0;
}
