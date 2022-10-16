## [B.Rebellion](https://codeforces.com/contest/1746/problem/B)
---
### Accepted solution
```C++
#include <bits/stdc++.h>
using namespace std;
 
void solve(){
    int n;
    cin >> n;
    vector<int> a(n);
    int count_zero = 0, count_one = 0;
    for (int i = 0; i < n; i++){
        cin >> a[i];
        if(a[i] == 0){
            count_zero++;
        }
        else{
            count_one++;
        }
    }
    
    if(count_zero == n || count_one == n){
        cout << 0 << "\n";
    }
    else{
        int front = 0, pointer_end = n - 1, move_count = 0;
        while(front < pointer_end){
                if(a[pointer_end] == 0){
                    if(a[front] == 1){
                            move_count++;
                            pointer_end--;
                        }
                    front++;
                    }
                else{
                    pointer_end--;
                }
            }
            cout << move_count << "\n";
        return;
    }
}
 
int main () {
    ios::sync_with_stdio(0);
    cin.tie(0);
    long long t;
    cin >> t;
    while(t--){
        solve();
    }
    return 0;
}
```
