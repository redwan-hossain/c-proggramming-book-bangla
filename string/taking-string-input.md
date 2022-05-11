# taking string input

scanf  দিয়ে string ইনপুট নিলে যখনই কোনো white-space পাবে তার পর থেকে আর প্রিন্ট হবে না কারণ  scanf Token অনুযায়ী ইনপুট নেয়। white-space মানে হলো end of a token. এই সমস্যা এড়াতে  scanf এর পরিবর্তে gets(array\_name); ব্যবহার করতে হয় যেটা দিয়ে নতুন লাইনের আগ পর্যন্ত প্রিন্ট করা যায় কারণ gets এর delimiter হলো new line.&#x20;

prevent buffer overflow = fgets

{% hint style="info" %}
নিচের কোড দিয়ে স্পেস দিয়ে কোন string প্রিন্ট হবে না।
{% endhint %}

```c
#include <stdio.h>

int main() {
  char string[100];
  scanf("%s", string);
  puts(string);
  return 0;
}
```



```c
#include <stdio.h>

int main() {
    char string[100];
    gets(string);
    puts(string);
    return 0;
}
```
