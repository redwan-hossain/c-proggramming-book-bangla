# array

Array একটি ডাটা স্ট্রাকচার যেখানে একই ডাটা টাইপের একাধিক ডাটা জমা করে রাখা যায়। ডাটা স্ট্রাকচার হলো একটা ফরম্যাট  যেখানে  নির্দিষ্ট উদ্দেশ্যের জন্য ডাটা organize এবং store করা হয়। Array তে একাধিক ডাটা chronologically রাখা হয় এবং অবশ্যই একই টাইপের ডাটা হতে হয়, মিশ্র ডাটা টাইপ array তে রাখা যায় না। array এর syntax নিচে দেয়া হলো- `data_type array_name[size]`

একটা কাজের জন্য অসংখ্য ভেরিয়েবল ডিক্লেয়ার করা কস্টসাধ্য, তাই array দিয়ে একাধিক ভেরিয়েবলের কাজ অনায়াসে করা যায়, কারণ array's প্রতিটা element স্বতন্ত্র ভেরিয়েবলের কাজ করে এবং মেমোরিতে element গুলো পাশাপাশি অবস্থান করে।

ধরা যাক, int ডাটা টাইপের array declare করা হলো যার সাইজ 5. তাহলে এই array এর জন্য int টাইপের 5 টা variable declare করলে যেটুকু যায়গা লাগতো ঠিক ততটুকুই এই array এর জন্য লাগবে। অন্যভাবে বলা যায় এই array টি পাঁচটা int টাইপের ভেরিয়েবলের মত কাজ করবে।  তাহলে মেমোরি এলোক্যাশন এর লজিক টা হবে নিম্নরুপ-`amount*sizeof(data_type)`

Array এর সাইজ নির্ধারণ করতে অবশ্যই positive integer ব্যবহার করতে হবে, কোনোরকম ভগ্নাংশ কিংবা ঋণাত্মক মান গ্রহণযোগ্য না। একটা array এর যত সহজ তাকে তত element এর array বলে, এবং প্রতিটা element এর নির্দিষ্ট index থাকে। Array index সবসময় শূন্য থেকে শুরু হয়।  তাই Array index এর লজিক হলো `length-1` Array element access করতে চাইলে`array_name[index_no]` এভাবে লিখতে হয়।&#x20;

Array size macros দিয়ে declare করা বেস্ট প্রাকটিস কারণ পরবর্তীতে কোডে array এর সাইজ পরিবর্তন করার প্রয়োজন হলে header এ থাকা macros থেকে সহজেই পরিবর্তন করা যায়। যেমন-

&#x20;`#define N 20`&#x20;

`int array1[N]`\


Array size থেকে কম এলিমেন্ট ইনপুট দিলে খালি জায়গাগুলো শূন্য দিয়ে ভরাট হবে। array size থেকে কখনোই বেশি element input দেয়া যাবেনা, এবং array input একদম খালি রাখা যাবেনা, কমপক্ষে একটা input দিতেই হবে।`int array5[10]={0};`এভাবে দিলে বাকি সেল গুলো শূন্য দিয়ে ভরাট হবে।



{% hint style="info" %}
Array দিয়ে N সংখ্যক বিষয়ের এভারেজ মার্ক বের করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>
int result, upto;

int main() {
  printf("Total sunject: ");
  scanf("%d", &upto);

  int grade[upto];

  for (int timer = 0; timer < upto; timer++) {
 printf("Enter subject %d score: ", timer+1);
    scanf("%d", &grade[timer]);
    result = result + grade[timer];
  }

  if (result > 0) {
    result = result / upto;
    printf("Average mark: %d \n", result);
  }

  return 0;
}
```
