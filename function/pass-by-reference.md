# pass by reference

array কে argument দিয়ে parameter এ pass করলে সেটা pass by reference হিসেবে যায় তাই user defined function এর ভেতরে array এর ভ্যালু manipulation হলে সেটা function এর বাইরেও এক্সেস করা যায়।&#x20;

```
#include "iostream"
#include "string"

using namespace std;

void trying(int *n) {
  *n = 20;
}

int main() {
  int n = 10;
  int *ptr = &n;
  trying(ptr);

  cout << n << endl;
}
```
