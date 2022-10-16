# 01. How to simply the question?
## Intro

We overthought for several questions in the training. One example is [E. Riana's Excruciating Enhancement Enigma](https://codeforces.com/gym/102556/problem/E) in [2020 Ateneo de Manila University DISCS PrO HS Division](https://codeforces.com/gym/102556)

We carried on with the discussion about the P&C and intermediate steps for this question and wasted about 1 hour. However, the answer is just x.

```C++
#include <iostream>
using namespace std;
int main() {
    long long v;
    cin >> v;
    cout << v << '\n';
}
```

For some other problems, we can try to simple and generalize the questions instead of manually create all the categories, which is unnecessary and easy to lead to error.