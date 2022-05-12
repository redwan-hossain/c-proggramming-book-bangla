# taking string input

scanf  দিয়ে string ইনপুট নিলে যখনই কোনো white-space পাবে তার পর থেকে আর প্রিন্ট হবে না কারণ  scanf Token অনুযায়ী ইনপুট নেয়। white-space মানে হলো end of a token. এই সমস্যা এড়াতে  scanf এর পরিবর্তে gets(array\_name); ব্যবহার করতে হয় যেটা দিয়ে নতুন লাইনের আগ পর্যন্ত প্রিন্ট করা যায় কারণ gets এর delimiter হলো new line.&#x20;

তবে gets ব্যবহার করা বিপদজনক কারণ এটা buffer overflow ঘটাতে পারে। যেমন: ধরা যাক একটা 5 ইলিমেন্টের array তে  gets দিয়ে ইনপুট নেয়া হবে, gets array এর সাইজ তোয়াক্কা না করে ইউজার থেকে ইনপুট নিতেই থাকবে যতক্ষণ পর্যন্ত তাকে দেয়া হবে এবং array এর সাইজ cross করলেই প্রোগ্রাম এমনকি সিস্টেমও ক্রাশ করতে পারে। buffer overflow এড়াতে <mark style="color:red;">`fgets`</mark> ব্যবহার করতে হয় যার সিনট্যাক্স gets থেকে কিছুটা ভিন্ন।&#x20;

<mark style="color:red;">`fgets(array_name, array_size, stdin);`</mark>

{% hint style="info" %}
নিচের কোড দিয়ে স্পেস দিয়ে কোন string প্রিন্ট হবে না।
{% endhint %}

```c
#include <stdio.h>

int main() {
  char string[10];
  scanf("%s", string);
  puts(string);
  return 0;
}
```

{% hint style="danger" %}
নিচের কোড gets দিয়ে লিখা হয়েছে যেটায় buffer overflow বাগ আছে।
{% endhint %}

```c
#include <stdio.h>

int main() {
    char string[10];
    gets(string);
    puts(string);
    return 0;
}
```

{% hint style="success" %}
নিচের কোডে gets এর পরিবর্তে fgets ব্যবহার করায় buffer overflow বাগ নেই।

fgets স্বয়ংক্রিয়ভাবে string এর শেষে null character যোগ করে দেয়।
{% endhint %}

```c
#include <stdio.h>

int main() {
    char string[10];
    fgets(string, 10, stdin);
    puts(string);
    return 0;
}
```
