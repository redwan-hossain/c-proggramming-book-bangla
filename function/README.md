# function

Code re-usability, easier debugging, less error prone ইত্যাদি সুবিধার জন্য function ব্যবহার করা হয়।&#x20;

dry- don't repeat yourself এই প্রিন্সিপাল function এর মাধ্যমে implement করা সম্ভব।&#x20;

{% hint style="success" %}
Function Design:
{% endhint %}

variable এর মতই function এর একটা identifier বা নাম দিতে হয় এবং naming conventions গুলো variable এর নিয়ম অনুযায়ীই হবে।&#x20;

function দিয়ে কোনো কাজ করিয়ে নেয়ার জন্য তাকে input দিতে হবে, এই input কে parameter/formal parameter বলা হয়।  অন্যভাবে বললে function declaration এবং definition এর সময়কার variable কে parameter বলে।&#x20;

function এর parameter কে function calling এর সময় argument দ্বারা value input দেয়া হয়। তাই Function call এর সময়কার variable কে argument/actual parameter বলে।

&#x20;function দিয়ে কাজ করানোর পর সে একটা ভ্যালু output হিসেবে return করবে, এজন্য function কোন ডাটা টাইপে return করবে সেটাও বলে দিতে হয়।

Function এর ভেতর আউটপুট দেয়া উচিত না, বরং function calling side এ আউটপুট দেয়া উচিত।

&#x20;একটা function কে শুধুমাত্র একটা কাজের জন্যই বরাদ্ধ রাখা উচিত এবং function এর নাম সেই কাজের জন্য অর্থবোধ্য হওয়া উচিত।





```c
#include <stdio.h>

int sumf(int a, int b) {
  int sum = a + b;
  return sum;
}  // function declaration and definition
   // it includes function prototype as well as definition

int subf(int, int);
// function declaration/prototype only

int main() {
  int digit1, digit2;

  scanf("%d %d", &digit1, &digit2);

  int sum = sumf(digit1, digit2);
  int sub = subf(digit1, digit2);
  // calling function and passing argument

  printf("sum-> %d sub-> %d\n", sum, sub);

  return 0;
}

int subf(int x, int y) {
  int left = x - y;
  return left;
}  // function declaration including definition
   // it is worthless because we are declaring function twice
   // only useful for calling function from different file
```

{% hint style="info" %}
function ব্যবহার করে n তম triangular number বের করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

int triangular_num(int n) {
  int sum = 0;
  for (int i = 1; i <= n; i++) {
    sum = sum + i;
    // it just adds 1 to num and prints the sum
    // example: if num=5, 1+2+3+4+5= 15
  }
  printf("%d\n", sum);
  return sum;
}

int main() {
  int num;
  scanf("%d", &num);
  triangular_num(num);
  // calling the function by passing argument through it

  return 0;
}
```

{% hint style="info" %}
function ব্যবহার করে factorial(up-to 65) বের করার প্রোগ্রাম:
{% endhint %}

```c
#include <stdio.h>

int factorial(int n) {
  unsigned long long multiply = 1;
  for (int i = n; i >= 1; i--) {
    multiply = multiply * i;
    // factorial calculator upto 65
  }
  printf("%llu\n", multiply);
  return multiply;
}

int main() {
  int num;
  scanf("%d", &num);
  factorial(num);
  // calling the function by passing argument through it

  return 0;
}
```
