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
int n;
cin>>n;

int arr[n];
for(int i=0;i<n;i++){
    cin>>arr[i];
}

int ans=2;
int pd= arr[1]-arr[0];
int j=2;
int curr=2;

while(j<n){
    if(pd==arr[j]-arr[j-1]){
        curr++;
    }
    else{
        pd=arr[j]-arr[j-1];
        curr = 2;
    }
    ans=max(ans,curr);
    j++;
}
cout<<ans<<endl;
    return 0;
}

