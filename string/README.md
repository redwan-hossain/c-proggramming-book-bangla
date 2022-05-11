# string

string হলো `""` এর ভেতর থাকা ক্যারেক্টারের সমষ্টি যাকে string literal বলা হয়ে থাকে। character এর সাথে এর পার্থক্য হলো character <mark style="color:red;">`''`</mark> এর ভেতর থাকে, অপরদিকে string অবশ্যই <mark style="color:red;">`""`</mark> এর ভেতর থাকে।

C তে string array এর ভেতর রাখতে হয় এবং string এর শেষে বাড়তি array element হিসেবে একটা null character `/0` থাকে যেটা string এর সমাপ্তি বুঝায় এবং null character যেখানেই থাকবে তার পর থেকেই string প্রিন্ট হওয়া বন্ধ হয়ে যাবে। এখানে লক্ষণীয় যে, <mark style="color:red;">`0`</mark> এবং <mark style="color:red;">`/0`</mark> এক নয়।

string এর মাঝে array element দিয়ে কোনো একটা character পরিবর্তন করতে চাইলে `''` এর ভেতর রেখে  লিখতে হবে কারণ এখানে আমরা একটা মাত্র character পরিবর্তন করতে যাচ্ছি, কোনো string না।&#x20;

যেমন:  `"Hello World."` এর 1 এবং 2 নং character পরিবর্তন করে আউটপুট `"Hallo World."`  করতে চাইলে <mark style="color:red;">`string[1] = 'a';`</mark> লিখতে হবে।&#x20;

string কে placeholder<mark style="color:red;">`%s`</mark> দিয়ে `printf` এর সাহায্যে প্রিন্ট করা যায়, এবং `puts(array_name);` দিয়েও প্রিন্ট করা যায়। মজার ব্যাপার হলো `puts(array_name);` দিয়ে প্রিন্ট করলে অটোম্যাটিক ভাবে নতুন লাইন যোগ হয়ে যায়।





{% hint style="info" %}
নিচের কোডের মত <mark style="color:red;">`\`</mark> দিয়ে মাল্টি লাইন string লিখতে চাইলে লাইনগুলোর মাঝখানের স্পেসগুলো কাউন্ট হবে। নিচের কোড টা লুপ ব্যবহার করে লিখা হয়েছে:
{% endhint %}

```c
#include <stdio.h>

int main() {
  char string[] =
      "Hello World.\
       This is new line.";

  int size = sizeof(string) / sizeof(string)[0];

  for (int i = 0; i < size; i++) {
    printf("%c", string[i]);
  }
  printf("\n");
  return 0;
}
```

{% hint style="info" %}
একই string <mark style="color:red;">`" " " "`</mark> আলাদা কোটেশন মার্কের ভেতর রাখলে অনাকাংখিত স্পেস আসবে না। নিচের কোড টা লুপের পরিবর্তে string এর placeholder<mark style="color:red;">`%s`</mark>ব্যবহার করে লিখা হয়েছে:
{% endhint %}

```c
#include <stdio.h>

int main() {
  char string[] =
      "Hello World. "
      "This is new line.";

  printf("%s", string);
  printf("\n");
  return 0;
}
```
