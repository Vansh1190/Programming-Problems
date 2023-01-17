<h1>This is the question</h1>
<samp>

<h3>Friends Or Not? !</h3>
Time Limit: 2 sec
Memory Limit: 128000 kB
Problem Statement
The students of Newton School threw a grand party to celebrate their hard work and achievements. They danced and sang the night away, enjoying delicious food and creating memories that would last a lifetime.
There are N guests in the party and N-1 relationships are given. The guests are numbered 1, 2,. , N. The i- th relationship depicts that guest ai and guest bi are friends.
Determine whether a guest exists or not who is a friend of all other guests.
Here, we only consider the direct friendship.
Input
Input is given from Standard Input in the following format:
<pre>
N

a1 b1
a2 b2
a3 b3
.
.
.
.
an-1 bn-1


Constraints
3 ≤ N ≤ 10^5
1 ≤ ai, bi ≤ N
i≤N
Output
If a guest exists or who is a friend of all other guests, print "Yes" else print "No".
Example
Sample Input 1
5
1 4
2 4
3 4
4 5

Sample Output 1
Yes

Sample Input 2
4
2 4
1 4
2 3

Sample Output 2
No

Sample Input 3
10
3 10
4 10
9 10
1 10
7 10
5 10
2 10
8 10
6 10

Sample Output 3
Yes
</pre>
</samp>



<h1>My solution for this problem is </h1>
<pre>
#include <bits/stdc++.h> // header file includes every Standard library
using namespace std;

int main() {
    int N;
	cin>>N;
    int R[N-1][2];
    for(int i=0;i<(N-1);i++){
        for(int j=0;j<2;j++){
            cin>>R[i][j];
        }
    }
    // checking test cases;
    int check;
    // cout<<check;
    int count;
for(int k=0;k<2;k++){
    count = 0;
        if(k==0){
             check = R[0][0];
        }
        else{
             check = R[0][1];
        }
        for(int i=0;i<(N-1);i++){
        for(int j=0;j<2;j++){
           if(check==R[i][j]){
               count++;
           }
          }
        }
    // cout<<count<<"IT is count"<<endl;
}
    if(count==(N-1)){
        cout<<"Yes";
    }
    else{
        cout<<"No";
    }
}

</pre>





