- š Hi, Iām @AnkurJain305
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
AnkurJain305/AnkurJain305 is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
using namespace std;
int revDigit(int y){
    int rem,rev=0;
    while(y>0){
        rem=y%10;
        rev=rev*10+rem;
        y/=10;
        
    }return rev;
}


bool isPalindrome(int x) {
    //complete the function
    if(x==revDigit(x)){
        return true;
    }
    else{
        return false;
    }
        
    

}

int main() {
    int n;
    cin >>n;
    
    if(isPalindrome(n)) {
        cout <<n<<" is a palindrome";
    }
    else {
        cout << n<<" is NOT a palindrome";
    }
    return 0;
}
