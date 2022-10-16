# Debug-04. What to do when we encounter test error?

We will have test error such as [C. Circuit Board Design](https://codeforces.com/gym/102483/problem/C) for [2018-2019 ICPC Northwestern European Regional Programming Contest (NWERC 2018)] (https://codeforces.com/gym/102483)

The code with error on test 3 is shown:
```C++
#include <bits/stdc++.h>
using namespace std;
 
#define INC 0.03
 
int main() {
    int n,a,b,c;
    double l;
    cin >> n;
    vector<vector<int>> graph(n);
    vector<pair<double,double>> coords(n);
    vector<double> angles(n);
    vector<bool> visited(n);
 
    while (--n) {
        cin >> a >> b;
        a--;
        b--;
        graph[a].emplace_back(b);
        graph[b].emplace_back(a);
    }
 
    stack<int> q;
    q.push(0);
    visited[0] = true;
    while (q.size()) {
        c = q.top();
        q.pop();
        auto v = coords[c];
        l = angles[c];
        for (auto i: graph[c]) {
            if (visited[i]) continue;
            l += INC;
            q.push(i);
            coords[i] = {v.first+cos(l), v.second+sin(l)};
            angles[i] = l;
            visited[i] = true;
        }
    }
    for (auto i: coords)
        printf("%.7lf %.7lf\n", i.first, i.second);
}
```

What can we do to solve this test error?