# static variable

সাধারণ variable কে automatic variable বলা হয় যেটা কাজ শেষে destroy হয়ে যায়। একইভাবে যখন একটা function এর কাজ শেষে তার মধ্যে সকল variable destroy হয়ে যায় এবং পরবর্তীতে function টিকে call করলে variable গুলো আবার তৈরি হয়। কিন্ত যে variable গুলো function এর ভেতর static variable হিসেবে declare করা হয় সেগুলো function এর কাজ শেষ হয়ে যাবার পরেও destroy না হয়ে নিজের ভ্যালু ধরে রাখে।

```cpp
#include "iostream"

using namespace std;

int func() {
  static int a = 0;
  ++a;
  return a;
}
int func2() {
  int a = 0;
  ++a;
  return a;
}

int main() {
  for (int i = 1; i <= 5; i++) {
    cout << func() << " ";
  }
  
  cout << endl;

  for (int i = 1; i <= 5; i++) {
    cout << func2() << " ";
  }

  return 0;
}
```
