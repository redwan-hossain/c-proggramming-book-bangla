# array

Array একটি ডাটা স্ট্রাকচার যেখানে একই ডাটা টাইপের একাধিক ডাটা জমা করে রাখা যায়। ডাটা স্ট্রাকচার হলো একটা ফরম্যাট  যেখানে  নির্দিষ্ট উদ্দেশ্যের জন্য ডাটা organize এবং store করা হয়। Array তে একাধিক ডাটা chronologically রাখা হয় এবং অবশ্যই একই টাইপের ডাটা হতে হয়, মিশ্র ডাটা টাইপ array তে রাখা যায় না। array এর syntax নিচে দেয়া হলো- `data_type array_name[size]`

একটা কাজের জন্য অসংখ্য ভেরিয়েবল ডিক্লেয়ার করা কস্টসাধ্য, তাই array দিয়ে একাধিক ভেরিয়েবলের কাজ অনায়াসে করা যায়, কারণ array's প্রতিটা element স্বতন্ত্র ভেরিয়েবলের কাজ করে এবং মেমোরিতে element গুলো পাশাপাশি অবস্থান করে।

ধরা যাক, int ডাটা টাইপের array declare করা হলো যার সাইজ 5. তাহলে এই array এর জন্য int টাইপের 5 টা variable declare করলে যেটুকু যায়গা লাগতো ঠিক ততটুকুই এই array এর জন্য লাগবে। অন্যভাবে বলা যায় এই array টি পাঁচটা int টাইপের ভেরিয়েবলের মত কাজ করবে।  তাহলে মেমোরি এলোক্যাশন এর লজিক টা হবে নিম্নরুপ-`amount*sizeof(data_type)`

Array এর সাইজ নির্ধারণ করতে অবশ্যই positive integer ব্যবহার করতে হবে, কোনোরকম ভগ্নাংশ কিংবা ঋণাত্মক মান গ্রহণযোগ্য না। একটা array এর যত সহজ তাকে তত element এর array বলে, এবং প্রতিটা element এর নির্দিষ্ট index থাকে। Array index সবসময় শূন্য থেকে শুরু হয় কারণ array zero index এ কাজ করে।  তাই Array index এর লজিক হলো `array_length-1` Array element access করতে চাইলে`array_name[index_no]` এভাবে লিখতে হয়।

Array size macros দিয়ে declare করা বেস্ট প্রাকটিস কারণ পরবর্তীতে কোডে array এর সাইজ পরিবর্তন করার প্রয়োজন হলে header এ থাকা macros থেকে সহজেই পরিবর্তন করা যায়। যেমন-

&#x20;`#define N 20`&#x20;

`int array1[N]`\


array size কে ডায়নামিক করতে চাইলে variable length array ব্যবহার করা যায়। এর মানে হলো array size এর জায়গায় একটা ভেরিয়েবল বসাতে হয় এবং scanf এর সাহায্যে ঐ ভেরিয়েবলের মান নির্ধারণ করলে array এর size টাও ঐ ভেরিয়েবলের সমান হবে। উদাহরণস্বরূপ:

```c
#include <stdio.h>


int main() {
 
   int size;
  
  scanf("%d", &size);

  int my_ array[size];

  return 0;
}
```

Array size থেকে কম এলিমেন্ট ইনপুট দিলে খালি জায়গাগুলো শূন্য দিয়ে ভরাট হবে। array size থেকে কখনোই বেশি element input দেয়া যাবেনা, এবং array input একদম খালি রাখা যাবেনা, কমপক্ষে একটা input দিতেই হবে।`int array5[10]={0};`এভাবে দিলে বাকি সেল গুলো শূন্য দিয়ে ভরাট হবে।

`sizeof(arr) / sizeof(arr[0])` দিয়ে একটা array এর সাইজ বের করা যায়, যেমন-&#x20;

```c
int arr[10]
sizeof(arr) / sizeof(arr[0])
// 40/4 = 10
```

![](../.gitbook/assets/array\_element\_count.png)

{% hint style="info" %}
Array তে 1 থেকে 5 সংখ্যাগুলো মোট কত বার আছে সেটা বের করতে চাইলে নিচের মত অনেকগুলো ভেরিয়েবল নিয়ে প্রোগ্রামটা লিখা যায়: &#x20;
{% endhint %}



```c
#include <stdio.h>

int users;
int one, two, three, four, five;

int main() {


    printf("Total users: ");
    scanf("%d", &users);

    int ratings[users];

    for (int i = 0; i < users; i++) {
        scanf("%d", &ratings[i]);
    }


    for (int i = 0; i < users; i++) {
        if (ratings[i] == 1) {
            one++;
        }
        if (ratings[i] == 2) {
            two++;
        }

        if (ratings[i] == 3) {
            three++;
        }
        if (ratings[i] == 4) {
            four++;
        }

        if (ratings[i] == 5) {
            five++;
        }
    }


    printf("%d %d %d %d %d\n", one, two, three, four, five);

    return 0;
}
```

{% hint style="info" %}
একই প্রোগ্রাম ভেরিয়েবলের পরিবর্তে একটামাত্র Array দিয়ে কাজটা করে ফেলা যায় যার পোগ্রাম নিচে দেয়া হলো:
{% endhint %}

```c
#include <stdio.h>

int users, test;
int count[6];
// index 0 is useless because input will be 1-5
// thats why we need 6 sized array

int main() {
  printf("Total users: ");
  scanf("%d", &users);

  int ratings[users];

  for (int i = 0; i < users; i++) {
    scanf("%d", &ratings[i]);
  }

  for (int i = 0; i < users; i++) {
    test = ratings[i];

    // test variable will point the index of count[6] array from 1-5
    // based on the loop and values of ratings[users] array
    // count[1]
    // count[2]
    // count[3]
    // count[4]
    // count[5]
    count[test] = count[test] + 1;
  }
  // when 1 is found, increase count[1] by 1.
  // again when 1 is found, increase count[1] by 1
  // count[1]'s value was 1, now it will be 1+1 = 2

  for (int i = 1; i <= 5; i++) {
    printf("%d -> %d \n", i, count[i]);
  }

  return 0;
}
```

{% hint style="info" %}
Array এর সব ইলিমেন্ট এর যোগফল বের করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

int n, timer, sum;

int main() {
    printf("Total digit: ");
    scanf("%d", &n);

    int arr[n];

    for (timer = 0; timer < n; timer++) {
        printf("Digit %d: ", timer + 1);
        scanf("%d", &arr[timer]);
        sum = sum + arr[timer];

    }

    if (sum >= 0) {
        printf("Total: %d", sum);
    }


    return 0;
}
```

{% hint style="success" %}
Array দিয়ে N সংখ্যক বিষয়ের এভারেজ মার্ক বের করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

int upto;
double result;
//double is used to handle average like 4+5= 9/2= 4.50

int main() {
    printf("Total sunject: ");
    scanf("%d", &upto);

    int grade[upto];

    for (int timer = 0; timer < upto; timer++) {
        printf("Enter subject %d score: ", timer + 1);
        scanf("%d", &grade[timer]);
        result = result + grade[timer];
    }

    if (result > 0) {
        result = (double) result / (double) upto;
        //explicit type casting 
        printf("Average mark: %lf \n", result);
    }

    return 0;
}
```

{% hint style="success" %}
N সংখ্যক নাম্বার ইনপুট নিয়ে রিভার্স অর্ডারে প্রিন্ট করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

int result, upto, timer;

int main() {
    printf("Total number: ");
    scanf("%d", &upto);

    int grade[upto];

    for (timer = 0; timer < upto; timer++) {
        printf("Digit %d: ", timer + 1);
        // +1 ensures the prompt start from digit 1, not 0
        scanf("%d", &grade[timer]);
    }

    for (timer = upto - 1; timer >= 0; timer--) {

        // without -1, there will be one extra array element
        // if array size is 2, the index will be 0 and 1 
        // without -1, this loop will run at 2, 1, 0
        // with the -1 hack, this loop will run at 1, 0
        
        printf("%d ", grade[timer]);
    }

    printf("\n");

    return 0;
}
```

{% hint style="success" %}
N(up-to 93) সংখ্যক ফিবোনাচ্চি সিরিজ বের করার প্রোগ্রাম :
{% endhint %}

```c
#include <stdio.h>

int main() {
  int upto;
  printf("Total digit: ");
  scanf("%d", &upto);

  long long fibonacci[upto];

  fibonacci[0] = 0;
  fibonacci[1] = 1;
  // the initial 2 values of fibonacci series are 0 and 1

  for (int timer = 2; timer < upto; timer++) {
    fibonacci[timer] = fibonacci[timer - 1] + fibonacci[timer - 2];
    // fibonacci means the sum of previous 2 digits
    // timer - 1 will provide the immediate previous digit
    // timer - 2 will provide the immediate previous of immediate previous digit
  }
  for (int timer = 0; timer < upto; timer++) {
    printf("%d--> %lld \n", timer + 1, fibonacci[timer]);
  }

  return 0;
}
```

{% hint style="info" %}
Array কে counter হিসেবে ব্যবহার করে 1-5 rating calculate করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

void main(void) {
  int n;
  scanf("%d", &n);
  int arr[n], temp;
  int count[6] = {0};

  for (int i = 0; i < n; i++) {
    scanf("%d", &arr[i]);
    temp = arr[i];
    ++count[temp];
  }
  for (int i = 1; i < 6; i++) {
    if (count[i] != 0) {
      printf("%d->  %d\n", i, count[i]);
    }
  }
}
```
