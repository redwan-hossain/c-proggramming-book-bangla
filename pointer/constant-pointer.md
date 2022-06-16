# constant pointer

একটা constant variable এর value সাধারণ ভাবে পরিবর্তন করা যায় না। কিন্ত চাইলে pointer এর de-reference operator দিয়ে constant variable এর value পরিবর্তন করা যায়।&#x20;

```c
#include <stdio.h>

int main() {
  const int n = 20;
  int *ptr = &n;
  *ptr = 9000;
  printf("%d \n", n);

  return 0;
}
```

কিন্ত pointer variable কেও যদি constant রাখা হয় তাহলে pointer দিয়েও value পরিবর্তন করা সম্ভব না। <mark style="color:red;">**`const int *ptr= &n;`**</mark>\
const pointer variable এর value হিসেবে থাকা মেমোরি এড্রেস চাইলে পরিবর্তন করা যায়। এটাও বন্ধ করতে চাইলে const pointer variable declare করার সময় \* এর পর const লিখে দিতে হবে। <mark style="color:red;">**`const int *const ptr= &n;`**</mark>

Array তে দ্বিতীয় টাইপের constant pointer ব্যবহৃত হয় কারণ এই constant pointer নিজের ভ্যালু পরিবর্তন করতে পারে না। এই কারণে লুপ দিয়ে একে increment/decrement করা যায় না।
