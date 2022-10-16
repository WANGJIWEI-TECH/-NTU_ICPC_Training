## [A.Maxmina](https://codeforces.com/contest/1746/problem/A)
---
### Accepted solution

```C++
#include <bits/stdc++.h>
using namespace std;
 
void solve(){
    int n, k;
    cin >> n >> k;
    vector<int> a(n);
    int flag = 0;
    for (int i = 0; i < n; i++){
        cin >> a[i];
        if (a[i] == 1)
            flag = 1;
    }
    if (flag == 1){
        cout << "YES" << "\n";
    }
    else{
        cout << "NO" << "\n";
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
