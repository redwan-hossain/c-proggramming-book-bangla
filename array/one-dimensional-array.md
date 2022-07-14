# one dimensional array

{% hint style="success" %}
array initialize বলতে array declare করার পর তার initial ভ্যালু assign করাকে বুঝায়।
{% endhint %}

{% hint style="info" %}
One dimensional array initialize করার নিয়ম-
{% endhint %}

array index এর value সেট করতে constant value বাদেও অন্যে variable এর নাম, expression, এবং function call করা যায়।

```cpp
#include "stdio.h"

int func(int n) {
  return n * n;
}

int main() {
  int num = 20;
  int arr[] = {num, func(2), 5 - 2};
  return 0;
}
```

```c
int array1[3]= {1,2,3};
```

```c
int array2[ ]= {1,2,3};
//সবথেকে ভালো, কারণ এখানে array size ফিক্সড না।
```

{% hint style="danger" %}
সেকেন্ড ব্র্যাকেটের ভেতর এইভাবে array element initialize করা এটা শুধুমাত্র array declare করার সময় করা যায়, অন্যসময় এভাবে সেকেন্ড ব্র্যাকেট ব্যবহার করা যায় না।
{% endhint %}

```c
int array3[2];
array3[0] = 1; 
array3[1] = 1;
//সবচেয়ে বাজে এবং বোরিং নিয়ম
```

```c
int array4[variable]; 
for (i=0; i<array4; i++){
scanf("%d", &array4[i]);
}
//যখন ইউজার ইনপুট নিয়ে ডায়নামিকভাবে array ইলিমেন্ট সেট করতে হয় তখন loop দিয়ে করা সুবিধা।
```



{% hint style="info" %}
Designated Initialization of array
{% endhint %}

ধরা যাক try নামে একটা array যেখানে ১০ টা element আছে `int try[10]`, এখন আমি 2 নং, 5 নং এবং 7 নং ইনডেক্সে ভ্যালু assign করবো এবং বাকি ইনডেক্স গুলোর ভ্যালু শূন্য থাকবে। সাধারণ নিয়মে এটা করা অসম্ভব মনে হলেও designated Initialization এর মাধ্যমে এই অসাধ্য সাধন করা সম্ভব। নিচে সিনট্যাক্স দেয়া হলো:

```c
int try[10] = {[2]=12, [5]=15, [7]=24};
```

এখানে সেকেন্ড ব্র্যাকেটের ভেতর থাকা থার্ড ব্র্যাকেটগুলোর মধ্যকার ভ্যালুগুলোকে designator বলা হয়। এভাবে array initialize করার সময় designator এর ক্রোনোলজি ঠিক না রাখলেও সমস্যা হয়না। array size ফিক্সড করে না দিলে সর্বোচ্চ designator ভ্যালু অনুযায়ী array size নির্ধারিত হবে।

traditional নিয়ম এবং Designated Initialization এর নিয়ম দুইটা মিক্সড করে array এর এলিমেন্ট ডিক্লেয়ার করা যায়। যদি দুইটার মধ্যে conflict হয় অর্থাৎ traditional declaration এবং designator একই index কে টার্গেট করে হয় তাহলে designator প্রাধান্য পাবে।

```c
int try[10] = {[2]=12, 50 [5]=15, [7]=24}, 65;
```

