# pointer

যখন কোনো একটা variable declare করা হয়  তখন তার জন্য data type অনুযায়ী মেমোরিতে জায়গা বরাদ্ধ করা হয়।&#x20;

যেমনঃ <mark style="color:red;">**`int x= 5;`**</mark> এখানে x এর জন্য 4 byte জায়গা বরাদ্ধ হবে, x এর কাছে শুধু প্রথম বাইট এর address টা থাকে, বাকিগুলো data type অনুযায়ী calculate করে নেয়া হয়। x এর range 100 থেকে 103 পর্যন্ত হবে। pointer variable এর কাজ হলো সে সাধারণ variable এর address store করে রাখে, আরো বিস্তারিত বললে শুধু প্রথম বাইট এর address টা store করে রাখে বাকিটা data type অনুযায়ী calculate করে নেয়।

{% hint style="info" %}
Syntax- <mark style="color:red;">`data_type *pointer_name`</mark>
{% endhint %}

{% hint style="warning" %}
মনে রাখতে হবে যখন asterik symbol<mark style="color:red;">`*`</mark> এর আশেপাশে যখন কোনো data type keyword থাকেনা তখন<mark style="color:red;">`*`</mark> এটাকে deteference operator বলে। deteference operator দিয়ে pointer যাকে point করছে তার value access করা হয়।
{% endhint %}

Pointer variable এর নিজস্ব data type থাকেনা । তাই pointer declare এর সময় যে `data_type` দিতে হয় সেটা মূলত pointer যাকে point করবে সেটার data\_type হয়। এই data type তাহলে কেন দরকার?  pointer variable এ শুধুমাত্র প্রথম বাইট এর address টা জমা থাকে। বাকি বাইট গুলোর হিসাব-নিকাশ করার জন্য data type দরকার হয় কারণ কোন variable কত বাইট সেটা data type দেখে বোঝা যায়। de-reference operator `*` দিয়ে pointer variable এ যে address জমা রাখা আছে সেই address এর ভ্যালু access করতে কাজে লাগে। যেমন:&#x20;

```c
#include <stdio.h>
int main() {
  int n = 10;
  
  int *p = &n;  
  // *p এর কাছে n এর এড্রেস আছে 
  
  *p = 20;      
  // এখানে dereference operator দিয়ে n এর ঘরে গিয়ে n কে update করে দেয়া হচ্ছে
  
  printf("%d\n", n);  // output is 20
  return 0;
}
```

pointer of pointer দিয়ে pointer এর chain বানানো যায়। যেমন: n এর address \*p তে থাকবে, \*p এর address \*q তে থাকবে। pointer q দিয়ে n এর value manipulate করতে চাইলে দুইটা de-reference operator `**` দিয়ে করতে হবে কারণ একটা দিলে সে pointer p তে point করবে, দুইটা দিলে n কে point করবে। এভাবে যত বড়  pointer এর chain হবে ততগুলো de-reference operator ব্যবহার করতে হবে।

```c
#include <stdio.h>
int main() {
  int n = 10;

  int *p = &n;
  *p = 20;  

  int **q = &p;  // pointer of pointer

  **q = 100;  // double dereference to manipulate variable n

  printf("%d \n", n); // output is 100
  return 0;
}
```
