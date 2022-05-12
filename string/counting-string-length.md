# counting string length

string array তে কতটা ক্যারেক্টার আছে সেটা খুব সহজেই <mark style="color:red;">`#include <string.h>`</mark> নামক লাইব্রেরীতে থাকা <mark style="color:red;">`strlen(array_name)`</mark> ফাংশন দিয়ে বের করে ফেলা যায়। প্রথমেই একটা int type ভেরিয়েবল ডিক্লেয়ার করতে হবে তারপর ভেরিয়েবলের ভ্যালু হিসেবে <mark style="color:red;">`strlen(array_name)`</mark> ফাংশন দিয়ে size টা assign করতে হবে। পরবর্তীতে ভেরিয়েবল টার ভ্যালু প্রিন্ট দিলেই string array তে কতটা ক্যারেক্টার আছে সেটা প্রিন্ট হয়ে যাবে।

{% hint style="info" %}
Note that the strlen() function doesn't count the null character \0 while calculating the length.
{% endhint %}

```c
#include <stdio.h>
#include <string.h>

int main() {
  char string[10];
  fgets(string, 10, stdin);
  puts(string);
  int length = strlen(string);
  // strlen(array_name) is used for finding the srtring length
  // length variable is used for storing character count in a string array 
  printf("%d\n", length);
  return 0;
}

```
