<h1>This is the question</h1>
<samp>

<h3>Even Numbers - 2</h3>
Time Limit: 2 sec
Memory Limit: 128000 kB
Problem Statement
Newton loves EVEN numbers.

You are given two integers N and M. Generate 5 unique even numbers for Newton between N and M (excluding both).
Input
The first and the only line of input contains integer N and integer M.


Constraints
-103 <= N <=M <= 103

M - N > 10
Output
The only line of output contains 5 singly spaced integers satisfying the constraints.
Example
Sample Input
0 20

Sample Output
2 6 8 18 14
</pre>
</samp>



<h1>My solution for this problem is </h1>
<pre>
#include <bits/stdc++.h> // header file includes every Standard library
using namespace std;

int main() {
	int n,m;
    cin>>n>>m;
    int count =0;
    for(int i=n+1;i<m;i++){
        if(count==5){
            break;
        }
        if(i%2==0){
            count++;
            cout<<i<<" ";
        }
    }
}

</pre>
